<script lang="ts">
  import type { Snippet } from "svelte";

  export let href: string;
  export let name: string;
  export let image: string;
  export let children: Snippet;
</script>

<a
  {href}
  class="group bg-card hover:bg-card/85 flex w-full flex-row justify-between rounded-3xl p-4 transition-all hover:rounded-xl sm:w-[480px] sm:gap-x-4"
>
  <div class="flex min-w-0 shrink-1 flex-col justify-start gap-4 p-2 sm:pr-1">
    <h3 class="text-2xl sm:text-2xl/6">{name}</h3>
    <span class="text-lg/6 break-words sm:text-xl/6"
      >{@render children?.()}</span
    >
  </div>

  <div
    class="transition-all flex h-36 w-36 shrink-0 items-center justify-center rounded-2xl group-hover:rounded-sm bg-white sm:h-44 sm:w-44"
  >
    <img
      src={image}
      class="h-[85%] w-[85%] object-contain"
      alt={name + " logo"}
    />
  </div>
</a>
