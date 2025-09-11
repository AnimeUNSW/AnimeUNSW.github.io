<script lang="ts">
  import { ChevronDown } from '@lucide/svelte';
  import { ChevronUp } from '@lucide/svelte';

  let open = false;

  function toggleAccordion() {
    open = !open;
  }

</script>

<!-- each indiviual item -->
<div class="flex relative right-0 w-[665px] h-16">
  <!-- div for text -->
  <div class="my-[13px] mx-[12px]">
    <span class="text-[24px]/[28px]">
      Can you go back to the old one?
    </span>
  </div>
  <button class="absolute right-0 top-1/2 -translate-y-1/2" on:click={toggleAccordion}>
    {#if open}
      <ChevronUp class="w-[42px] h-[42px]"/>
    {:else}
      <ChevronDown class="w-[42px] h-[42px]"/>
    {/if}
  </button>
</div>

{#if open}
  <div class="mb-3 ml-3 w-[599px] text-wrap">
    <span class="text-xl/6 ">No! You’re stuck looking at this mess, deal with it, loser. If you’d like to file a complaint please send me a message on Discord at @soidjfoiefoisjfe (real) and I’ll see what I can do!</span>
  </div>
{/if}
