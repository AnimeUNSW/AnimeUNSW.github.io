<script lang="ts">
  export let icon: IconVariant;
  export let label: string;
  export let href: string;

  import { Icon, type IconVariant } from "$lib/components/ui/icon";
  import { MediaQuery } from "svelte/reactivity";

  const md = new MediaQuery("min-width: 768px");
</script>

<a
  {href}
  aria-label={label}
  class="bg-primary hover:bg-primary/95 flex h-16 w-16 items-center justify-center rounded-2xl transition-all hover:rounded-lg md:h-12 md:w-12"
>
  <Icon variant={icon} fill="white" size={md.current ? 24 : 30} />
</a>
