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
  const sponsorImageModules = import.meta.glob("$lib/assets/sponsors/*.png", {
    eager: true,
  });
  import sponsors from "$lib/assets/sponsors/sponsors.json";

  const randomSponsors = () => {
    const shuffled = Object.entries(sponsorImageModules).sort(
      () => Math.random() - 0.5,
    );
    return shuffled.slice(0, 6);
  };

  let scrollY;

  import { browser } from "$app/environment";
</script>

<svelte:head>
  <title>AnimeUNSW</title>
</svelte:head>

<div class="relative">
  <div class="h-[512px] w-screen overflow-hidden bg-black md:h-[768px]">
    <div
      class="p-[10vw 20vw] bg-position-[center 25%] box-border h-full w-full bg-[url($lib/assets/home/desert.png)] bg-cover bg-no-repeat opacity-60"
      style="transform: translateY({scrollY * 0.25}px);"
    ></div>
  </div>
  <div
    class="absolute -bottom-5 flex w-full items-center justify-center lg:-bottom-3 xl:-bottom-1"
  >
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
  <div
    class="absolute -bottom-5 z-10 flex w-full items-center justify-center lg:-bottom-3 xl:-bottom-1"
  >
    <img src={ibi_fg} alt="Ibi" class="w-[200px] md:w-[300px]" />
  </div>
  <div
    class="absolute top-0 left-0 z-20 flex h-full w-full flex-col items-center justify-center space-y-4 pb-8 text-white md:pb-64"
    style="transform: translateY({scrollY * 0.125}px);"
  >
    <h1 class="text-4xl font-bold min-[400px]:text-5xl md:text-7xl">
      「AnimeUNSW」
    </h1>
    <h2 class="text-xl min-[436px]:text-2xl md:text-3xl">
      A few of us happen to like anime! (嘘)
    </h2>
  </div>
</div>
<div class="bg-background relative flex items-center justify-center pb-4">
  <div
    class="mt-8 flex w-full flex-col space-y-8 self-center md:space-y-16 md:px-8 lg:w-[1152px]"
  >
    <div
      class="flex flex-col items-center justify-between space-y-8 md:flex-row md:space-x-8"
    >
      <div class="flex w-full flex-col space-y-2 px-6 md:max-w-[448px] md:px-0">
        <h2 class="text-3xl">About</h2>
        <p class="text-justify text-lg/6">
          A society formed by students with a passion in anime/manga that has
          continued to run exciting events both online and IRL. We’re always
          giving away prizes for competitions/raffles so stay tuned!! We’ve
          grown into one of Sydney’s biggest anime clubs! Memberships are open
          to anyone, as we strive to gather students interested in anime/manga
          to socialise and form friendships.
        </p>
      </div>
      <div
        class="z-20 grid min-w-fit grid-cols-2 gap-2 pb-8 min-[724px]:grid-cols-4 md:grid-cols-2 md:pb-0"
      >
        <SocialCard icon="discord" href="https://discord.gg/aunsw"
          >3200+ Members</SocialCard
        >
        <SocialCard icon="instagram" href="https://instagram.com/animeunsw"
          >2200+ Followers</SocialCard
        >
        <SocialCard icon="facebook" href="https://www.facebook.com/unswanime/"
          >1700+ Followers</SocialCard
        >
        <SocialCard
          icon="xiaohongshu"
          href="https://www.xiaohongshu.com/user/profile/67dd3a43000000000d0095f5"
          >140+ Followers</SocialCard
        >
      </div>
    </div>
    <div
      class="flex flex-col items-center justify-between space-y-8 md:flex-row md:space-x-12"
    >
      <div class="flex w-full items-center justify-center md:max-w-[448px]">
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
      <div class="flex w-full flex-col space-y-2 px-6 md:max-w-[448px] md:px-0">
        <h2 class="text-3xl">Events</h2>
        <p class="text-justify text-lg/6">
          We have a bunch of cool events and I haven’t been to most of them!!!!
          Wow!
        </p>
      </div>
    </div>
    <div
      class="flex flex-col-reverse items-center justify-between space-y-8 space-y-reverse md:flex-row md:space-x-8"
    >
      <div class="flex w-full flex-col space-y-2 px-6 md:max-w-[448px] md:px-0">
        <h2 class="text-3xl">Perks</h2>
        <p class="text-justify text-lg/6">
          As a member with us, you also unlock access to countless discounts
          from our valued sponsors, as well as discounts to our larger events
          including major parties.
        </p>
      </div>
      <div
        class="flex w-full items-center justify-center md:max-w-[448px] md:min-w-[448px] md:justify-start"
      >
        <div
          class="grid h-fit w-fit grid-cols-3 items-center justify-center gap-2 px-2 md:px-0"
        >
          {#if browser}
            {#each randomSponsors() as [path, module]}
              <a
                href={sponsors[path.substring(path.lastIndexOf("/") + 1)].url}
                class="flex aspect-square h-full w-full items-center justify-center rounded-3xl bg-white p-4 transition-all hover:rounded-xl hover:bg-white/85 sm:h-32 sm:w-32"
              >
                <img
                  src={module.default}
                  alt={sponsors[path.substring(path.lastIndexOf("/") + 1)].name}
                  class="h-[85%] w-[85%] object-contain"
                />
              </a>
            {/each}
          {/if}
        </div>
      </div>
    </div>
  </div>
</div>
<div class="bg-card relative h-56">
  <div
    class="absolute top-2 flex w-full items-center justify-center md:top-4 lg:top-6"
  >
    <img src={feet} alt="Ibi" class="ml-32 w-[106px] md:ml-48 md:w-[159px]" />
  </div>
  <svg
    viewBox="0 0 1440 58"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    width="100%"
    class="absolute top-0 bg-transparent"
    ><path
      d="M-100 58C-100 58 218.416 36.3297 693.5 36.3297C1168.58 36.3297 1487 58 1487 58V-3.8147e-06H-100V58Z"
      fill="var(--background)"
    ></path></svg
  >
  <div
    class="absolute bottom-0 flex w-full flex-row items-end justify-between p-4"
  >
    <p>
      Developed and maintained by <a
        href="https://github.com/rin-senpai"
        class="text-primary underline">Rin</a
      >
    </p>
    <Icon variant="arc" size={69} fill="var(--foreground)" />
  </div>
</div>

<svelte:window bind:scrollY />
