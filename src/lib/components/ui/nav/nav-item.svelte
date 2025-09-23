<script lang="ts">
  export let href: string;
  export let label: string;
  export let scrollY = 0;

  import { page } from "$app/state";
</script>

<li class="group relative w-fit">
  <span
    class={[
      "absolute -inset-1 -top-2 -right-4 -bottom-[6px] -left-4 inline-block rounded-full transition-all group-hover:text-white",
      page.url.pathname === href
        ? "opacity-100"
        : "opacity-0 group-hover:opacity-8 dark:group-hover:opacity-15",
      page.url.pathname === "/" && scrollY <= 100
        ? "bg-white group-hover:opacity-15"
        : "bg-secondary",
    ]}
    aria-hidden="true"
  ></span>
  <span class="relative">
    <a
      {href}
      class={[
        "text-2xl transition-all md:text-2xl md:font-bold",
        page.url.pathname === href
          ? "text-secondary-foreground"
          : page.url.pathname === "/" && scrollY <= 100
            ? "text-foreground md:text-white"
            : "text-foreground",
      ]}>{label}</a
    >
  </span>
</li>
