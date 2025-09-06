<script lang="ts">
  import up_arrow from "$lib/assets/arrow_drop_up.png"
  import Button from "./ui/button/button.svelte";
  import discord from "$lib/assets/discord.png"
  import insta from "$lib/assets/instagram.png"
  import fb from "$lib/assets/facebook.png"
  import xhs from "$lib/assets/xiaohongshu.png"
</script>

<Button class="absolute top-0 right-0 bg-[#FFFFFF] hover:bg-[#FFFFFF] text-2xl/[28px] text-black flex flex-col w-[279px] h-[128px] font-newcm">
  <div class="flex justify-between w-[279px]">
    <span>
      Join
    </span>
    <img src={up_arrow} alt="">
  </div>

  <div class="flex gap-x-[8px]">
    <div class="w-[56px] h-[56px]">
      <img src={discord} alt="">
    </div>

    <div class="w-[56px] h-[56px]">
      <img src={insta} alt="">
    </div>

    <div class="w-[56px] h-[56px]">
      <img src={fb} alt="">
    </div>

      <div class="w-[56px] h-[56px]">
      <img src={xhs} alt="">
    </div>
  </div>
</Button>