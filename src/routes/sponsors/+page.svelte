<script>
  import { SponsorCard } from "$lib/components/ui/card";
  import animeAtAbbotsford from "$lib/assets/sponsors/anime_at_abbotsford.png";
  import hamakonoBurwood from "$lib/assets/sponsors/hamakono_burwood.png";
  import harajukuGyoza from "$lib/assets/sponsors/harajuku_gyoza.png";
  import hobbyCo from "$lib/assets/sponsors/hobbyco.png";
  import isekaiGacha from "$lib/assets/sponsors/isekai_gacha.png";
  import kingpin from "$lib/assets/sponsors/kingpin.png";
  import mangaMate from "$lib/assets/sponsors/manga_mate.png";
  import patchesParadise from "$lib/assets/sponsors/patches_paradise.png";
  import sugoicoAU from "$lib/assets/sponsors/sugoico_au.png";
  import viaArtists from "$lib/assets/sponsors/via_artists.png";
  import genshinWhales from "$lib/assets/sponsors/genshin_whales.png";
  import hamaFilmCabramatta from "$lib/assets/sponsors/hama_film_cabramatta.png";
  import hondrarake from "$lib/assets/sponsors/hondrarake.png";
  import icedTeaAesthetics from "$lib/assets/sponsors/iced_tea_aesthetics.png";
  import itoEn from "$lib/assets/sponsors/ito_en.png";
  import japanFoundation from "$lib/assets/sponsors/japan_foundation.svg";
  import kahweiei from "$lib/assets/sponsors/kahweiei.png";
  import luminsWorkshop from "$lib/assets/sponsors/lumins_workshop.png";
  import redBull from "$lib/assets/sponsors/red_bull.svg";
  import rollWithAdvantage from "$lib/assets/sponsors/roll_with_advantage.png";
  import saigonBrew from "$lib/assets/sponsors/saigon_brew.png";
  import secondsPlease from "$lib/assets/sponsors/seconds_please.png";
  import sugoToys from "$lib/assets/sponsors/sugo_toys.svg";
  import wutaBistro from "$lib/assets/sponsors/wuta_bistro.png";
</script>

<svelte:head>
  <title>Sponsors | AnimeUNSW</title>
</svelte:head>

<div
  class="mt-3 mb-8 flex flex-wrap justify-center gap-3 px-4 md:mt-8 md:gap-6"
>
  <SponsorCard
    href="https://www.anime-oz.com/"
    name="Anime at Abbotsford"
    image={animeAtAbbotsford}>10% with membership card</SponsorCard
  >
  <SponsorCard
    href="https://www.instagram.com/hamakono_burwood/"
    name="HamaKono Burwood"
    image={hamakonoBurwood}
    ><span class="text-sm/4 break-words sm:text-xl/6">
      $5 cash only discount on photobooths & bonus 10 minutes ($5 value) added
      to karaoke
    </span></SponsorCard
  >
  <SponsorCard
    href="https://www.harajukugyoza.com/"
    name="Harajuku Gyoza"
    image={harajukuGyoza}>20% off Monday - Friday</SponsorCard
  >
  <SponsorCard href="https://www.hobbyco.com.au/" name="HobbyCo" image={hobbyCo}
    >10% off by showing member card at their stores</SponsorCard
  >
  <SponsorCard
    href="https://isekaianime.com.au/"
    name="Isekai Gacha"
    image={isekaiGacha}
    >Use code: <span class="font-mono">anisyd5</span> for 5% off</SponsorCard
  >
  <SponsorCard href="http://www.kingpinplay.com/" name="Kingpin" image={kingpin}
    >Prizes upon request</SponsorCard
  >
  <SponsorCard
    href="https://mangamate.shop/"
    name="Manga Mate"
    image={mangaMate}
    ><span class="text-sm/4 break-words sm:text-xl/6">
      10% online discount code: <span class="font-mono">animesydney</span> & 20%
      online discount code: <span class="font-mono">animesydney20</span> for first
      purchase
    </span></SponsorCard
  >
  <SponsorCard
    href="https://patchesparadise.com/"
    name="Patches Paradise"
    image={patchesParadise}
    >Use code: <span class="font-mono">ANIMESYDNEY</span> for $30 off only in March
    and October</SponsorCard
  >
  <SponsorCard
    href="https://www.facebook.com/sugoicoau/"
    name="Sugoico AU"
    image={sugoicoAU}
    >Provides movie tickets for AUNSW events/giveaways</SponsorCard
  >
  <SponsorCard
    href="https://viaartists.com/"
    name="Via Artists"
    image={viaArtists}
    >Use code: <span class="font-mono">ANISYD25</span> for 10% off, members show
    card for 10% in person discount</SponsorCard
  >

  <!-- I have to fix up the below logos!!!! -->
  <SponsorCard
    href="https://www.genshinwhales.com.au/"
    name="Genshin Whales"
    image={genshinWhales}
    >Use code: <span class="font-mono">ANIMESYDNEY5</span> for 5% off</SponsorCard
  >
  <SponsorCard
    href="https://www.instagram.com/hamakono_cabramatta/"
    name="Hama Film Cabramatta"
    image={hamaFilmCabramatta}
    ><span class="text-sm/4 break-words sm:text-xl/6"
      >Use code: <span class="font-mono">ANISYD25</span> for 10% off, members show
      card for 10% in person discount</span
    ></SponsorCard
  >
  <SponsorCard
    href="https://fullofbooks.com.au/"
    name="Hondrarake"
    image={hondrarake}
    >Bonus 10 minutes added to karaoke experiences & vouchers</SponsorCard
  >
  <SponsorCard
    href="https://www.it-aesthetics.com/"
    name="Iced Tea Aesthetics"
    image={icedTeaAesthetics}
    ><span class="text-xs/2 break-words sm:text-sm/4"
      >Use codes: <span class="font-mono">ANIMESYD</span> for 10% off,
      <span class="font-mono">ANIMESYD20</span>
      for 20% off (3+ items), <span class="font-mono">ANIMESYDEMB</span> for 20%
      off (embroidered collection),
      <span class="font-mono">ANIMESYDSHIP</span> for free shipping</span
    ></SponsorCard
  >
  <SponsorCard href="https://itoen.com.au/" name="ITO EN" image={itoEn}
    >Provides drinks for events</SponsorCard
  >
  <SponsorCard
    href="https://www.jpf.go.jp/e/"
    name="Japan Foundation"
    image={japanFoundation}
    ><span class="text-sm/4 break-words sm:text-xl/6"
      >Provides movie giveaways & event space, other JP promotions</span
    ></SponsorCard
  >
  <SponsorCard href="https://kahweiei.com/" name="Kahweiei" image={kahweiei}
    >Use code: <span class="font-mono">ANISYD10</span> for 10% off</SponsorCard
  >
  <SponsorCard
    href="https://www.luminsworkshop.com/"
    name="Lumin's Workshop"
    image={luminsWorkshop}
    ><span class="text-sm/4 break-words sm:text-xl/6"
      >Provide prizes for events and offers limited-time discounts for special
      events</span
    ></SponsorCard
  >
  <SponsorCard href="https://www.redbull.com/" name="Red Bull" image={redBull}
    >Provides drinks for events</SponsorCard
  >
  <SponsorCard
    href="https://rollwithadvantage.com.au/"
    name="Roll With Advantage"
    image={rollWithAdvantage}>Provides prizes for events</SponsorCard
  >
  <SponsorCard
    href="https://saigonbrew.com.au/"
    name="Saigon Brew"
    image={saigonBrew}>Provides drinks for events</SponsorCard
  >
  <SponsorCard
    href="https://secondsplease.jp/"
    name="Seconds Please!"
    image={secondsPlease}
    >Use code: <span class="font-mono">UNSW2025</span> for 10% off</SponsorCard
  >
  <SponsorCard
    href="https://sugotoys.com.au/"
    name="Sugo! Toys"
    image={sugoToys}
    >Provides prizes for events, and sometimes give discounts</SponsorCard
  >
  <SponsorCard
    href="https://www.instagram.com/wutabistro_syd/"
    name="Wuta Bistro"
    image={wutaBistro}>Members show card for 10% in person discount</SponsorCard
  >
</div>
