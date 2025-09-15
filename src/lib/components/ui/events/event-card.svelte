<script lang="ts">
  const furina = "https://media.assettype.com/afkgaming%2F2023-07%2F4cb3f3da-90dd-48bf-8258-46dd1b98bbc2%2FGenshin_Impact_Focalors_1.jpg?auto=format%2Ccompress&dpr=1.0&w=1200"
  let {largeImage, line} = $props();
</script>

<div class="flex flex-col md:w-[453px] w-[376px] p-4 gap-y-3 bg-white rounded-3xl">
  <!-- image -->
  <div class={`w-full h-[198px] ${largeImage ? 'md:h-[281px]' : 'md:h-[237px]'}`}>
    <img src={furina} alt="" class="w-full h-full object-cover rounded-lg">
  </div>
  <p class="md:w-[421px] w-[352px] md:text-xl/6 text-base/5 p-1">{line}</p>
</div>