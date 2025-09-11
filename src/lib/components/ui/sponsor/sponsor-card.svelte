<script lang="ts">
  import { Icon } from "$lib/components/ui/icon";
</script>

<!-- todo: fix hardcoded text and pictures later -->
 <!-- desktop design -->
<div class="flex w-[455px] h-[208px] justify-between p-6 rounded-3xl gap-x-6 bg-white items-center hidden md:flex">
  <!-- column 1 -->
  <div class="flex flex-col w-[217px] h-40 gap-4">
    <h3 class="text-2xl leading-[28px]">Durin :emote:</h3>
    <!-- todo: migt need to change the line height to match the figma -->
    <span class="break-words text-xl leading-[24px]">Use code DurinLetMedoUnspeakableThingsToYou at checkout for 99% off!</span>
  </div>

  <!-- column 2, image -->
  <div class="flex w-43 h-43 rounded-[15px] items-center bg-[#E9DEEC]">
    <Icon variant="discord" class="w-full h-full" />
  </div>
</div>

<!-- mobile design -->
<div class="flex w-[376px] h-[174px] justify-between p-5 rounded-3xl gap-x-[9px] bg-white items-center md:hidden">
  <!-- column 1 -->
  <div class="flex flex-col w-[189px] h-31 gap-4">
    <h3 class="text-[28px]/[28px]">Durin :emote:</h3>
    <span class="break-words text-base leading-[20px]">Use code DurinLetMedoUnspeakableThingsToYou at checkout for 99% off!</span>
  </div>

  <!-- column 2, image -->
  <div class="flex w-[142px] h-[142px] rounded-2xl items-center bg-[#E9DEEC]">
    <Icon variant="discord" class="w-full h-full" />
  </div>
</div>