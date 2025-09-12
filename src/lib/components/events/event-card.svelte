<script lang="ts">
  import durin from "$lib/assets/durin.svg"
  let {largeImage, line} = $props();
</script>

<div class="flex flex-col w-[453px] p-4 gap-y-[12px] bg-white rounded-3xl flex-grow-0">
  <!-- image -->
  <div class={`w-[421px] ${largeImage ? 'h-[281px]' : 'h-[237px]'}`}>
    <img src={durin} alt="" class="w-full h-full object-cover rounded-lg">
  </div>
  <p class="w-[421px] text-xl/6 p-1">{line}</p>
</div>