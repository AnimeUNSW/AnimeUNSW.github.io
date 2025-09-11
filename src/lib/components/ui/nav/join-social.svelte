<script lang="ts">
  export let icon: string;
  export let label: string;
  export let href: string;

  import { Icon } from "$lib/components/ui/icon";
  import { MediaQuery } from "svelte/reactivity";

  const md = new MediaQuery("min-width: 768px");
</script>

<a
  {href}
  aria-label={label}
  class="bg-primary hover:bg-primary/95 flex h-16 w-16 items-center justify-center rounded-2xl md:h-12 md:w-12"
>
  <Icon variant={icon} fill="white" size={md ? 24 : 30} />
</a>
