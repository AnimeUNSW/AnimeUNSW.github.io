<script lang="ts">
  import sampleImage from "../../lib/assets/discord.png"
</script>


<div class="flex w-[455px] h-[208px] justify-between p-[24px] rounded-[24px] bg-white">
  <!-- column 1 -->
  <div class="flex flex-col w-[217px] h-[160px] gap-[16px]">
    <h3 class="text-[24px]/[28px]">Durin :emote:</h3>
    <span class="break-words text-[20px]/[24px]">Use code DurinLetMedoUnspeakableThingsToYou at checkout for 99% off!</span>
  </div>

  <!-- column 2, image -->
  <!-- image should be 172 by 172 px, 15 corner radius -->
  <div class="flex w-[172px] h-[172px] rounded-[15px] items-center">
    <img class="w-full h-full object-cover" src={sampleImage} alt="">
  </div>
</div>