<script lang="ts">
  export let icon: string;
  export let numberFollowers: string;
  import { Icon } from "$lib/components/ui/icon";
  import { MediaQuery } from "svelte/reactivity";

  const md = new MediaQuery("min-width: 768px");
</script>

<div class="flex items-center bg-card w-55 h-24 p-2 pr-4 gap-4 rounded-3xl">
  <!-- todo: find right pink colour -->
  <div class="flex bg-pink-400 items-center justify-center w-20 h-20 rounded-2xl">
    <Icon variant={icon} fill="white" size={42} />
  </div>
  
  <span class="text-wrap text-2xl w-24">
    {numberFollowers}
  </span>
</div>