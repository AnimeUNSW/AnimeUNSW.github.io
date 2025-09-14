<script lang="ts">
  import type { Snippet } from "svelte";

  export let header: string;
  export let children: Snippet;
</script>

<div
  class="bg-card flex flex-col justify-center gap-y-4 rounded-3xl p-5 md:w-96 md:p-7"
>
  <h3 class="text-xl">{header}</h3>
  <p class="text-md text-justify md:text-xl/6">
    {@render children?.()}
  </p>
</div>
