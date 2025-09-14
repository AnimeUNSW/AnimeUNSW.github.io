<script>
  import { SponsorCard } from "$lib/components/ui/card";
  import animeAtAbbotsford from "$lib/assets/anime_at_abbotsford.png";
  import hamakonoBurwood from "$lib/assets/hamakono_burwood.png";
  import harajukuGyoza from "$lib/assets/harajuku_gyoza.png";
  import hobbyCo from "$lib/assets/hobbyco.png";
  import isekaiGacha from "$lib/assets/isekai_gacha.png";
  import kingpin from "$lib/assets/kingpin.png";
  import mangaMate from "$lib/assets/manga_mate.png";
  import patchesParadise from "$lib/assets/patches_paradise.png";
  import sugoicoAU from "$lib/assets/sugoico_au.png";
  import viaArtists from "$lib/assets/via_artists.png";
</script>

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
    >$5 cash only discount on photobooths & bonus 10 minutes ($5 value) added to
    karaoke</SponsorCard
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
    >10% online discount code: <span class="font-mono">animesydney</span> & 20%
    online discount code: <span class="font-mono">animesydney20</span> for first
    purchase</SponsorCard
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
</div>
