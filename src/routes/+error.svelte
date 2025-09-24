<script lang="ts">
  import { page } from "$app/state";
  import suffering from "$lib/assets/error/404.png";
</script>

<div
  class="flex min-h-[calc(100vh-72px)] w-full flex-col items-center justify-center space-y-8 md:min-h-[calc(100vh-68px)]"
>
  {#if page.status === 404}
    <h1 class="text-4xl font-bold">You seem lost!</h1>
  {:else}
    <h1 class="text-4xl font-bold">Error {page.status}</h1>
  {/if}
  <img src={suffering} alt="Sad Ibi" class="max-h-96 max-w-96" />
  {#if page.status === 404}
    <h2 class="text-xl">Page not found</h2>
  {:else}
    <h2 class="text-xl">{page.error.message}</h2>
  {/if}
</div>
