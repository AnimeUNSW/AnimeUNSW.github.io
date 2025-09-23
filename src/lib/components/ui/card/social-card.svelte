<script lang="ts">
  import type { Snippet } from "svelte";

  export let icon: IconVariant;
  export let href: string;
  export let children: Snippet;

  import { Icon, type IconVariant } from "$lib/components/ui/icon";
  import { MediaQuery } from "svelte/reactivity";

  const md = new MediaQuery("min-width: 768px");
</script>

<a
  {href}
  class="group bg-card hover:bg-card/85 flex w-43 items-center gap-4 rounded-3xl p-2 pr-4 transition-all hover:rounded-xl md:w-55"
>
  <div
    class="bg-primary flex h-14 w-14 items-center justify-center rounded-2xl group-hover:rounded-lg transition-all md:h-20 md:w-20"
  >
    <Icon variant={icon} fill="white" size={md.current ? 36 : 24} />
  </div>

  <span class="w-19 text-lg/5 text-wrap md:w-24 md:text-2xl">
    {@render children?.()}
  </span>
</a>
