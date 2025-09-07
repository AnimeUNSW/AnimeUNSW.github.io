<script>
  import Navbar from "../../lib/components/navbar.svelte"
  import SponsorCard from "../../lib/components/sponsor_card.svelte";
</script>


<div class="bg-[#E9DEEC] min-h-screen">
  <Navbar pageName="Sponsors"></Navbar>

  <!-- todo: remove the need to create two separate divs for mobile and desktop later if possible -->
  <!-- sponsor box (desktop)-->
  <div class="flex justify-center w-full hidden md:flex">
    <div class="w-[934px] font-newcm flex flex-wrap gap-[24px]">
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
    </div>
  </div>

  <!-- sponsor box mobile -->
  <div class="flex justify-center w-full md:hidden">
    <div class="w-[376px] font-newcm flex flex-wrap gap-y-[12px]">
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
    </div>
  </div>

</div>



