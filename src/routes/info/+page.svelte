<script>
  import InfoCard from "$lib/components/info_card.svelte";
</script>

<div>
  <div class="flex flex-col gap-y-[64px]">
    <div>
      Accordion frame
    </div>

    <!-- contact box frame 2 -->
    <div class="flex flex-col w-[822px] h-388px] gap-y-[70px] justify-center">
      <h2 class="text-[36px]/[28px] text-center">Want to contact us?</h2>
      <div class="flex gap-x-[32px]">
        <InfoCard></InfoCard>
        <InfoCard></InfoCard>
      </div>
    </div>
  </div>

</div>
