<script lang="ts">
  import "../app.css";
  let { children } = $props();
  import { Nav } from "$lib/components/ui/nav";
</script>

<link
  rel="stylesheet"
  type="text/css"
  href="https://cdn.jsdelivr.net/gh/dreampulse/computer-modern-web-font@master/fonts.css"
/>

<Nav />
{@render children()}
