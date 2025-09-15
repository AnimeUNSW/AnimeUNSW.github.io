<script lang="ts">
  import { EventCard } from "$lib/components/ui/events";
  const shortText = "AUNSW member in the wild"
  const longText = shortText + " but longer text real wow I love multiple lines mhmh true and real"
</script>

<!-- outer div -->
<div class="flex md:mt-8 mt-[14px] justify-center">
  <div class="flex w-full max-w-* md:gap-6 gap-3">
    <!-- masonry style -->
    <div class="columns-1 lg:columns-2 gap-3 md:gap-6 justify-center md:mt-8 mt-[14px] mx-auto [&>div:not(:first-child)]:mt-3 md:[&>div:not(:first-child)]:mt-6">
        <EventCard largeImage={false} line={shortText}/>
        <EventCard largeImage={true} line={longText}/>
        <EventCard largeImage={true} line={longText}/>
        <EventCard largeImage={false} line={shortText}/>
    </div>
  </div>
</div>