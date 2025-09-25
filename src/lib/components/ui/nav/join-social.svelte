<script lang="ts">
  export let icon: IconVariant;
  export let label: string;
  export let href: string;
  export let big = false;
  export let left = false;
  export let right = false;

  import { Icon, type IconVariant } from "$lib/components/ui/icon";
  import { MediaQuery } from "svelte/reactivity";

  const md = new MediaQuery("min-width: 768px");
</script>

<a
  {href}
  aria-label={label}
  target="_blank"
  class={[
    "bg-primary hover:bg-primary/95 flex h-16 items-center justify-center rounded-2xl transition-all hover:rounded-t-lg md:h-12",
    !left ? "hover:rounded-bl-lg" : "",
    !right ? "hover:rounded-br-lg" : "",
    big ? "xs:w-32 w-24 md:w-full" : "w-16 md:w-12",
  ]}
>
  <Icon
    variant={icon}
    fill="white"
    size={big ? (md.current ? 56 : 60) : md.current ? 24 : 30}
  />
</a>
