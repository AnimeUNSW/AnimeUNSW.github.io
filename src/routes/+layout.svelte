<script lang="ts">
  import "../app.css";
  import { ModeWatcher } from "mode-watcher";
  import { Nav } from "$lib/components/ui/nav";
  let { children } = $props();
</script>

<link
  rel="stylesheet"
  type="text/css"
  href="https://cdn.jsdelivr.net/gh/dreampulse/computer-modern-web-font@master/fonts.css"
/>

<ModeWatcher />
<Nav />
{@render children()}
