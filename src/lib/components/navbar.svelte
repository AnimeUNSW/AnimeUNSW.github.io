<script lang="ts">

  export let pageName: string = "";

  import aunswLogo from "$lib/assets/aunsw_logo.png"
  import mobileDownArrow from "$lib/assets/mobile_arrow_down.png"
  import mobileUpArrow from "$lib/assets/mobile_arrow_up.png"
  import discord from "$lib/assets/discord.png"
  import instagram from "$lib/assets/instagram.png"
  import facebook from "$lib/assets/facebook.png"
  import xiaohongshu from "$lib/assets/xiaohongshu.png"
  import JoinButton from "$lib/components/join_button.svelte";
  import JoinButtonExpanded from "$lib/components/join_button_expanded.svelte";
  import { fade } from 'svelte/transition';
  import { Button } from "./ui/button";

  let showSocials = false;
  let mobileArrowActivate = false;

  function toggleMobileNavbarButton() {
    mobileArrowActivate = !mobileArrowActivate;
  }

</script>

<!-- desktop design -->
<div class="flex items-start justify-between px-[24px] py-[16px] hidden lg:flex font-newcm">

  <!-- vertically center the image -->
  <div class="flex items-center h-[54.87px] w-[48px]">
    <img class="object-contain" src={aunswLogo} alt="">
  </div>


  <!-- 36 px of white space between elements -->
  <!-- text have a size of 24 px and 28px line height -->
  <ul class="flex space-x-9 text-2xl/[28px] font-bold">
    <li class="hover:underline">
        {#if pageName === "Events"}
          <Button class="text-2xl/[28px]">Events</Button>
        {:else}
          <a href="/events">Events</a>
        {/if}
    </li>
    <li class="hover:underline">
        {#if pageName === "Sponsors"}
          <Button class="text-2xl/[28px]">Sponsors</Button>
        {:else}
          <a href="/sponsors">Sponsors</a>
        {/if}
    </li>
    <li class="hover:underline">
        {#if pageName === "Info"}
          <Button class="text-2xl/[28px]">Info</Button>
        {:else}
          <a href="/info">Info</a>
        {/if}
    </li>
    <li class="hover:underline">
        {#if pageName === "Blog"}
          <Button class="text-2xl/[28px]">Blog</Button>
        {:else}
          <a href="/blog">Blog</a>
        {/if}
    </li>
  </ul>

  <!-- utilise a flag whenever hovering over -->
  <!-- svelte-ignore a11y-no-static-element-interactions -->
  <div
    onmouseenter={() => (showSocials = true)}
    onmouseleave={() => (showSocials = false)}
  >
    {#if !showSocials}
    <div transition:fade class="ease-in-out">
      <JoinButton/>
    </div>
    {:else if showSocials}
      <div transition:fade class="ease-in-out">
        <JoinButtonExpanded/>
      </div>
    {/if}
  </div>
</div>

<!-- mobile design -->
<div class="flex flex-col lg:hidden px-[16px] pb-24px gap-y-[16px] font-newcm">

  <!-- first row -->
  <div class="flex justify-between py-[16px] items-center">
    <div class="flex items-center h-[41px] w-[36px]">
      <img class="object-contain" src={aunswLogo} alt="">
    </div>
    
    {#if pageName}
      <span class="text-[32px]">{pageName}</span>
    {/if}

    <button class="flex items-center h-[42px] w-[42px]" onclick={toggleMobileNavbarButton}>
      <img class="object-contain" src={mobileArrowActivate ? mobileUpArrow : mobileDownArrow} alt="">
    </button>
  </div>

  {#if mobileArrowActivate}
  <div transition:fade class="ease-in-out">

    <div class="flex flex-col text-[24px] line-height-[28px] pl-[16px] w-max">

        {#if pageName === "Events"}
          <Button class="text-2xl/[28px]">Events</Button>
        {:else}
          <a href="/events" class="hover:underline">Events</a>
        {/if}

        {#if pageName === "Sponsors"}
          <Button class="text-2xl/[28px]">Sponsors</Button>
        {:else}
          <a href="/sponsors" class="hover:underline">Sponsors</a>
        {/if}


        {#if pageName === "Info"}
          <Button class="text-2xl/[28px]">Info</Button>
        {:else}
          <a href="/info" class="hover:underline">Info</a>
        {/if}

      {#if pageName === "Blog"}
        <Button class="text-2xl/[28px]">Blog</Button>
      {:else}
        <a href="/blog" class="hover:underline">Blog</a>
      {/if}

    </div>

    <!-- social media box -->
    <div class="flex px-[18px] pt-[16px] justify-between">
      <div class="w-[66px] h-[66px]">
        <img src={discord} alt="">
      </div>

      <div class="w-[66px] h-[66px]">
        <img src={instagram} alt="">
      </div>

      <div class="w-[66px] h-[66px]">
        <img src={facebook} alt="">
      </div>

      <div class="w-[66px] h-[66px]">
        <img src={xiaohongshu} alt="">
      </div>

    </div>
  </div>

  {/if}

</div>