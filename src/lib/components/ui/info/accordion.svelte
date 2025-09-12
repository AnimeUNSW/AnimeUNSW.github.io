<script lang="ts">
  import { ChevronDown } from '@lucide/svelte';
  import { ChevronUp } from '@lucide/svelte';

  let open = false;

  function toggleAccordion() {
    open = !open;
  }

</script>

<!-- each indiviual item -->
<div class="flex relative right-0 md:w-[665px] h-16 w-[362px]">
  <!-- div for text -->
  <div class="md:my-[13px] md:mx-3 mx-3 my-4">
    <span class="md:text-2xl/7 text-xl/7">
      Can you go back to the old one?
    </span>
  </div>
  <button class="absolute right-0 top-1/2 -translate-y-1/2" on:click={toggleAccordion}>
    {#if open}
      <ChevronUp class="md:w-[42px] md:h-[42px] w-[32px] h-[32px]"/>
    {:else}
      <ChevronDown class="md:w-[42px] md:h-[42px] w-[32px] h-[32px]"/>
    {/if}
  </button>
</div>

{#if open}
  <div class="mb-3 ml-3 md:w-[599px] w-[322px] text-wrap">
    <span class="md:text-xl/6 text-lg/5">No! You’re stuck looking at this mess, deal with it, loser. If you’d like to file a complaint please send me a message on Discord at @soidjfoiefoisjfe (real) and I’ll see what I can do!</span>
  </div>
{/if}
