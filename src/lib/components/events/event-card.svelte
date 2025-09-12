<script lang="ts">
  import durin from "$lib/assets/durin.svg"
  let {largeImage, line} = $props();
</script>

<div class="flex flex-col md:w-[453px] w-[376px] p-4 gap-y-3 bg-white rounded-3xl">
  <!-- image -->
  <div class={`md:w-[421px] w-[352px] h-[198px] ${largeImage ? 'md:h-[281px]' : 'md:h-[237px]'}`}>
    <img src={durin} alt="" class="w-full h-full object-cover rounded-lg">
  </div>
  <p class="md:w-[421px] w-[352px] md:text-xl/6 text-base/5 p-1">{line}</p>
</div>