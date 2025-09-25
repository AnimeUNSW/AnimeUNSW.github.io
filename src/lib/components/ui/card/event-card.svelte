<script lang="ts">
  import type { Snippet } from "svelte";

  export let image: string;
  export let alt: string;
  export let children: Snippet;
</script>

<div
  class="bg-card mb-2 inline-flex w-full flex-col gap-y-3 rounded-3xl p-3 align-top md:mb-6 md:p-4"
>
  <enhanced:img
    src={image}
    alt={alt}
    class="w-full rounded-xl object-cover md:rounded-lg"
  />
  <p class="p-1 text-base/5 md:text-xl/6">{@render children?.()}</p>
</div>
