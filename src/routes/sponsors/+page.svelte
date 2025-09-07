<script>
  import Navbar from "../../lib/components/navbar.svelte"
  import SponsorCard from "../../lib/components/sponsor_card.svelte";
</script>


<div class="bg-[#E9DEEC] min-h-screen">
  <Navbar pageName="Sponsors"></Navbar>
  <!-- sponsor box -->

  <div class="flex justify-center w-full">
    <div class="w-[934px] font-newcm flex flex-wrap gap-[24px]">
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
      <SponsorCard></SponsorCard>
    </div>
    
  </div>

</div>



