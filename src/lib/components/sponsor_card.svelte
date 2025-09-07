<script lang="ts">
  import sampleImage from "../../lib/assets/discord.png"
</script>


<!-- todo: fix hardcoded text and pictures later -->
 <!-- desktop design -->
<div class="flex w-[455px] h-[208px] justify-between p-[24px] rounded-[24px] gap-x-[24px] bg-white items-center hidden md:flex">
  <!-- column 1 -->
  <div class="flex flex-col w-[217px] h-[160px] gap-[16px]">
    <h3 class="text-[24px]/[28px]">Durin :emote:</h3>
    <span class="break-words text-[20px]/[24px]">Use code DurinLetMedoUnspeakableThingsToYou at checkout for 99% off!</span>
  </div>

  <!-- column 2, image -->
  <div class="flex w-[172px] h-[172px] rounded-[15px] items-center">
    <img class="w-full h-full object-cover" src={sampleImage} alt="">
  </div>
</div>

<!-- mobile design -->
<div class="flex w-[376px] h-[174px] justify-between p-[24px] rounded-[24px]  gap-x-[9px] bg-white items-center md:hidden">
  <!-- column 1 -->
  <div class="flex flex-col w-[189px] h-[124px] gap-[16px]">
    <h3 class="text-[28px]/[28px]">Durin :emote:</h3>
    <span class="break-words text-[16px]/[20px]">Use code DurinLetMedoUnspeakableThingsToYou at checkout for 99% off!</span>
  </div>

  <!-- column 2, image -->
  <div class="flex w-[142px] h-[142px] rounded-[16px] items-center">
    <img class="w-full h-full object-cover" src={sampleImage} alt="">
  </div>
</div>