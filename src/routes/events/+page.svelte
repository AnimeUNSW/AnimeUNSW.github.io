<script lang="ts">
  import { EventCard } from "$lib/components/ui/card";
  const eventImageModules = import.meta.glob(
    "$lib/assets/events/*.{png,jpg,jpeg}",
    {
      eager: true,
      query: {
        enhanced: true,
      },
    },
  );
  import events from "$lib/assets/events/events.json";

  const ordering = {
    "kickoff.jpg": 0,
    "social.jpg": 1,
    "challenges.jpg": 2,
    "trivia.jpg": 3,
    "things.jpg": 4,
    "cosplay.jpg": 5,
    "anisyd.jpg": 6
  }
  const sortedEvents = Object.entries(eventImageModules).sort((a, b) => ordering[a[0].substring(a[0].lastIndexOf("/") + 1)] - ordering[b[0].substring(b[0].lastIndexOf("/") + 1)]);

  import { browser } from "$app/environment";
</script>

<svelte:head>
  <title>Events | AnimeUNSW</title>
</svelte:head>

<div class="mt-3 mb-8 flex w-full justify-center items-center px-2 md:mt-8 md:px-8">
  <div
    class="w-full columns-1 gap-x-2 sm:columns-2 md:gap-x-6 xl:columns-3 2xl:w-[1472px] text-left"
  >
    {#if browser}
        {#each sortedEvents as [path, module]}
        <EventCard image={module.default} alt={events[path.substring(path.lastIndexOf("/") + 1)].alt}>{events[path.substring(path.lastIndexOf("/") + 1)].description}</EventCard>
        {/each}
    {/if}
  </div>
</div>
