<script lang="ts">
  import up_arrow from "$lib/assets/arrow_drop_up.png";
  import Button from "./ui/button/button.svelte";
  import discord from "$lib/assets/discord.png";
  import insta from "$lib/assets/instagram.png";
  import fb from "$lib/assets/facebook.png";
  import xhs from "$lib/assets/xiaohongshu.png";
</script>

<Button
  class="font-newcm absolute top-0 right-0 flex h-[128px] w-[279px] flex-col bg-[#FFFFFF] text-2xl/[28px] text-black hover:bg-[#FFFFFF]"
>
  <div class="flex w-[279px] justify-between">
    <span> Join </span>
    <img src={up_arrow} alt="" />
  </div>

  <div class="flex gap-x-[8px]">
    <div class="h-[56px] w-[56px]">
      <img src={discord} alt="" />
    </div>

    <div class="h-[56px] w-[56px]">
      <img src={insta} alt="" />
    </div>

    <div class="h-[56px] w-[56px]">
      <img src={fb} alt="" />
    </div>

    <div class="h-[56px] w-[56px]">
      <img src={xhs} alt="" />
    </div>
  </div>
</Button>
