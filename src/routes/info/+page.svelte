<script>
  import InfoCard from "$lib/components/ui/info/info-card.svelte";
  import Accordion from "$lib/components/ui/info/accordion.svelte";
</script>

<div class="md:mt-[67px] mt-[14px] flex justify-center">
  <div class="md:w-[882px] w-[362px]">
    <div class="flex flex-col md:gap-y-16 gap-y-8 items-center">
      <div class="md:w-[665px]">
        <Accordion />
        <Accordion />
        <Accordion />
      </div>

      <!-- contact box frame 2 -->
      <div class="flex flex-col md:h-[388px] md:gap-y-[70px] gap-y-4 justify-center">
        <h2 class="md:text-4xl/7 text-[32px]/7 text-center">Want to contact us?</h2>
        <div class="flex flex-wrap md:gap-x-8 gap-y-4">
          <InfoCard></InfoCard>
          <InfoCard></InfoCard>
        </div>
      </div>
    </div>
  </div>

</div>
