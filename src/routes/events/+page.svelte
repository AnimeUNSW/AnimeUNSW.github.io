<script lang="ts">
  import { EventCard } from "$lib/components/ui/events";
  const shortText = "AUNSW member in the wild"
  const longText = shortText + " but longer text real wow I love multiple lines mhmh true and real"
</script>

<!-- outer div -->
<div class="flex md:mt-8 mt-[14px] justify-center">
  <div class="flex flex-wrap md:w-[930px] w-[376px] md:gap-6 gap-3 items-start">
    <!-- had to use 2 separate columns because the sizing of the cards would get stretched -->
    <!-- todo: find a way to not use 2 separate divs? -->
    <!-- column 1 -->
    <div class="flex flex-col md:gap-6 gap-3">
      <EventCard largeImage={false} line={shortText}/>
      <EventCard largeImage={true} line={longText}/>
    </div>

    <!-- column 2 -->
    <div class="flex flex-col md:gap-6 gap-3">
      <EventCard largeImage={true} line={longText}/>
      <EventCard largeImage={false} line={shortText}/>
    </div>
  </div>
</div>