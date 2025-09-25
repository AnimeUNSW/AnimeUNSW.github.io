<script lang="ts">
  import { EventCard } from "$lib/components/ui/card";
  import { Button } from "$lib/components/ui/button";
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
    "anisyd.jpg": 6,
  };
  const sortedEvents = Object.entries(eventImageModules).sort(
    (a, b) =>
      ordering[a[0].substring(a[0].lastIndexOf("/") + 1)] -
      ordering[b[0].substring(b[0].lastIndexOf("/") + 1)],
  );

  import { browser } from "$app/environment";
</script>

<svelte:head>
  <title>Events | AnimeUNSW</title>
</svelte:head>

<div
  class="mt-3 mb-4 flex w-full items-center justify-center px-2 md:mt-8 md:px-8"
>
  <div
    class="w-full columns-1 gap-x-2 text-left sm:columns-2 md:gap-x-6 xl:columns-3 2xl:w-[1472px]"
  >
    {#if browser}
      {#each sortedEvents as [path, module]}
        <EventCard
          image={module.default}
          alt={events[path.substring(path.lastIndexOf("/") + 1)].alt}
          >{events[path.substring(path.lastIndexOf("/") + 1)]
            .description}</EventCard
        >
      {/each}
    {/if}
  </div>
</div>
<div class="flex items-center justify-center pb-8">
  <a
    href="https://campus.hellorubric.com/?s=12432"
    target="_blank"
    class="bg-primary hover:bg-primary/85 rounded-3xl px-4 py-2 text-xl transition-all hover:rounded-xl"
    >All Events</a
  >
</div>
