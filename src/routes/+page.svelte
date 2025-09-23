<script>
  import { SocialCard } from "$lib/components/ui/card";
  import * as Carousel from "$lib/components/ui/carousel";
  import { Icon } from "$lib/components/ui/icon";
  import desert from "$lib/assets/home/desert.png";
  import ibi_fg from "$lib/assets/home/ibi_fg.png";
  import ibi_bg from "$lib/assets/home/ibi_bg.png";
  import feet from "$lib/assets/home/feet.png";

  const eventImageModules = import.meta.glob(
    "$lib/assets/events/*.{png,jpg,jpeg}",
    {
      eager: true,
      query: {
        enhanced: true,
      },
    },
  );
  const sponsorImageModules = import.meta.glob(
    "$lib/assets/sponsors/*.png",
    {
      eager: true,
    },
  );

  const randomSponsors = () => {
    const shuffled = Object.entries(sponsorImageModules).sort(() => Math.random() - 0.5);
    return shuffled.slice(0, 6);
  };

  let scrollY;
</script>

<svelte:window bind:scrollY />

<svelte:head>
    <title>AnimeUNSW</title>
</svelte:head>

<div class="relative -z-10">
    <div class="bg-black md:h-[768px] h-[512px] w-screen overflow-hidden">
        <div class="bg-[url($lib/assets/home/desert.png)] h-full w-full box-border p-[10vw 20vw] opacity-60 bg-cover bg-no-repeat bg-position-[center 25%]" style="transform: translateY({scrollY * 0.25}px);"></div>
    </div>
  <div class="absolute -bottom-5 lg:-bottom-3 xl:-bottom-1 flex w-full items-center justify-center">
    <img src={ibi_bg} alt="Ibi" class="w-[200px] md:w-[300px]" />
  </div>
  <svg
    viewBox="0 0 1440 58"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    width="100%"
    class="absolute -bottom-1 rotate-180 bg-transparent"
    ><path
      d="M-100 58C-100 58 218.416 36.3297 693.5 36.3297C1168.58 36.3297 1487 58 1487 58V-3.8147e-06H-100V58Z"
      fill="var(--background)"
    ></path></svg
  >
  <div class="absolute -bottom-5 lg:-bottom-3 xl:-bottom-1 flex w-full items-center justify-center">
    <img src={ibi_fg} alt="Ibi" class="w-[200px] md:w-[300px]" />
  </div>
  <div
    class="absolute top-0 left-0 flex h-full w-full flex-col items-center justify-center space-y-4 pb-8 md:pb-64 text-white"
    style="transform: translateY({scrollY * 0.125}px);"
  >
    <h1 class="text-4xl min-[400px]:text-5xl md:text-7xl font-bold">「AnimeUNSW」</h1>
    <h2 class="text-xl min-[436px]:text-2xl md:text-3xl">A few of us happen to like anime! (嘘)</h2>
  </div>
</div>
<div class="flex justify-center items-center pb-4 bg-background relative -z-20">
    <div class="mt-8 flex flex-col space-y-8 md:space-y-16 md:px-8 w-full lg:w-[1152px] self-center">
      <div class="flex flex-col md:flex-row items-center justify-between space-y-8 md:space-x-8">
        <div class="flex w-full md:max-w-[448px] flex-col space-y-2 px-6 md:px-0">
          <h2 class="text-3xl">About</h2>
          <p class="text-justify text-lg/6">
            We do a few things like animeing and animeing yeah that’s all. Oh! Also
            we anime which is pretty cool yk you ever anime’d before it’s kinda
            crazy just like me haha ikr that’s funny I’m funny please laugh me when
            I don’t lorum ipsem mhm yep yeah true yeah
          </p>
        </div>
        <div class="grid min-w-fit grid-cols-2 min-[724px]:grid-cols-4 md:grid-cols-2 gap-2">
          <SocialCard icon="discord" href="https://discord.gg/aunsw"
            >3200+ Members</SocialCard
          >
          <SocialCard icon="instagram" href="https://instagram.com/animeunsw"
            >2200+ Followers</SocialCard
          >
          <SocialCard icon="facebook" href="https://www.facebook.com/unswanime/"
            >1700+ Followers</SocialCard
          >
          <SocialCard icon="xiaohongshu" href="https://www.xiaohongshu.com/user/profile/67dd3a43000000000d0095f5"
            >10+ Followers</SocialCard
          >
        </div>
      </div>
      <div class="flex flex-col md:flex-row items-center justify-between space-y-8 md:space-x-12">
        <div class="flex w-full md:max-w-[448px] justify-center items-center">
            <Carousel.Root class="w-full max-w-64">
            <Carousel.Content>
                {#each Object.entries(eventImageModules) as [_path, module]}
                <Carousel.Item>
                    <enhanced:img src={module.default} alt="owo" class="w-64" />
                </Carousel.Item>
                {/each}
            </Carousel.Content>
            <Carousel.Previous />
            <Carousel.Next />
            </Carousel.Root>
        </div>
        <div class="flex w-full md:max-w-[448px] flex-col space-y-2 px-6 md:px-0">
          <h2 class="text-3xl">Events</h2>
          <p class="text-justify text-lg/6">
            We have a bunch of cool events and I haven’t been to most of them!!!! Wow!
          </p>
        </div>
      </div>
      <div class="flex flex-col-reverse md:flex-row items-center justify-between space-y-reverse space-y-8 md:space-x-8">
        <div class="flex w-full md:max-w-[448px] flex-col space-y-2 px-6 md:px-0">
          <h2 class="text-3xl">Perks</h2>
          <p class="text-justify text-lg/6">
            We have a bunch of cool perks like idk sponsor discounts wow so cool!!!!!!!!!!!!
          </p>
        </div>
        <div class="flex w-full md:min-w-[448px] md:max-w-[448px] items-center justify-center md:justify-start">
            <div class="justify-center items-center grid grid-cols-3 gap-2 w-fit h-fit md:px-0 px-2">
                {#each randomSponsors() as [_path, module]}
                    <div class="w-full h-full aspect-square sm:w-32 rounded-3xl p-4 sm:h-32 bg-white flex items-center justify-center">
                        <img src={module.default} alt="owo" class="h-[85%] w-[85%] object-contain" />
                    </div>
                {/each}
            </div>
        </div>
      </div>
    </div>
</div>
<div class="bg-card relative h-56">
    <div class="absolute top-2 md:top-4 lg:top-6 flex w-full items-center justify-center">
      <img src={feet} alt="Ibi" class="ml-48 w-[106px] md:w-[159px]" />
    </div>
    <svg
      viewBox="0 0 1440 58"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
      width="100%"
      class="bg-transparent absolute top-0"
      ><path
        d="M-100 58C-100 58 218.416 36.3297 693.5 36.3297C1168.58 36.3297 1487 58 1487 58V-3.8147e-06H-100V58Z"
        fill="var(--background)"
      ></path></svg
    >
    <div class="absolute bottom-0 w-full flex flex-row justify-between p-4 items-end">
        <p>Developed and maintained by <a href="https://github.com/rin-senpai" class="text-primary underline">Rin</a></p>
        <Icon variant="arc" size={69} fill="var(--foreground)" />
    </div>
</div>
