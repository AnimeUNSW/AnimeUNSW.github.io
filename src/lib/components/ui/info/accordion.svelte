<script lang="ts">
  import { ChevronDown } from '@lucide/svelte';
</script>

<!-- outer accordion -->
 <!-- todo: remove size hard coding later -->
<div class="w-[665px] h-[276px]">
  <!-- each indiviual item -->
  <div class="flex relative right-0 w-[665px] h-[64px] outline-dashed">
    <!-- div for text -->
    <div class="my-[13px] mx-[12px]">
      <span class="text-[24px]/[28px]">
        Why is your website ugly?
      </span>
    </div>
    <ChevronDown class="absolute right-0 top-1/2 -translate-y-1/2 w-[42px] h-[42px]"/>
  </div>
</div>