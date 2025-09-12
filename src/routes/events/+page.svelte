<script lang="ts">
  import EventCard from "$lib/components/events/event-card.svelte";

  const shortText = "AUNSW member in the wild"

  const longText = shortText + " but longer text real wow I love multiple lines mhmh true and real"
</script>

<!-- outer div -->
<div class="flex mt-8 justify-center">
  <div class="flex flex-wrap w-[930px] gap-6 items-start">
    <EventCard largeImage={false} line={shortText}/>
    <EventCard largeImage={true} line={longText}/>
    <EventCard largeImage={true} line={longText}/>
    <EventCard largeImage={true} line={longText}/>
  </div>
</div>