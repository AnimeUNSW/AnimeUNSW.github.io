<script lang="ts">
  import { Icon } from "$lib/components/ui/icon";
  import Facebook from "$lib/assets/facebook.png";
  import droolingCat from "$lib/assets/drooling-cat.svg";
</script>

<div class="flex w-[376px] h-[174px] justify-between p-5 rounded-3xl gap-x-[9px] bg-white items-center md:w-[455px] md:h-[208px] md:p-6 md:rounded-3xl md:gap-x-6">
  <!-- column 1 -->
  <div class="flex flex-col w-[189px] h-31 gap-4 md:w-[217px] md:h-40 md:gap-4">
    <h3 class="text-[28px]/[28px] md:text-2xl md:leading-[28px]">Durin :emote:</h3>
    <span class="break-words text-base leading-[20px] md:text-xl md:leading-[24px]">Use code DurinLetMedoUnspeakableThingsToYou at checkout for 99% off!</span>
  </div>

  <!-- column 2, image -->
  <div class="flex w-[142px] h-[142px] rounded-2xl items-center justify-center bg-[#E9DEEC] md:w-43 md:h-43 md:rounded-[15px]">
    <img src={droolingCat} class="w-full h-full object-contain" alt="">
  </div>
</div>