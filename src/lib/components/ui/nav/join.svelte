<script lang="ts">
  import { ChevronUp, ChevronDown } from "@lucide/svelte";
  import JoinSocial from "./join-social.svelte";
</script>

<button
  class="group bg-primary text-primary-foreground relative rounded-full pt-2 pr-3 pb-[6px] pl-4"
>
  <div class="flex flex-row items-center space-x-3">
    <p class="text-lg">Join</p>
    <ChevronDown />
  </div>
  <div
    class="bg-primary group-hover:bg-card invisible absolute top-0 right-0 flex h-[42px] w-[97.2px] flex-col rounded-[21px] pt-2 pb-[6px] transition-all duration-200 ease-in-out group-hover:visible group-hover:h-[98px] group-hover:w-[222px]"
  >
    <div class="flex flex-row items-center justify-between space-x-3 pr-3 pl-4">
      <p class="text-card-foreground text-lg">Join</p>
      <ChevronDown
        class="transition-transform duration-200 group-hover:rotate-180"
      />
    </div>
    <div
      class="flex flex-row items-center space-x-[6px] px-[6px] pt-2 opacity-0 transition-all group-hover:opacity-100"
    >
      <JoinSocial
        icon="discord"
        label="Discord"
        href="https://discord.gg/aunsw"
      />
      <JoinSocial
        icon="instagram"
        label="Instagram"
        href="https://instagram.com/animeunsw"
      />
      <JoinSocial
        icon="facebook"
        label="Facebook"
        href="https://www.facebook.com/unswanime/"
      />
      <JoinSocial
        icon="xiaohongshu"
        label="RedNote"
        href="https://discord.gg/aunsw"
      />
    </div>
  </div>
</button>
