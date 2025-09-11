<script lang="ts">
  export let href: string;
  export let label: string;

  import { page } from "$app/state";
</script>

<li class="group relative w-fit">
  <span
    class={[
      "bg-secondary absolute -inset-1 -top-2 -right-4 -bottom-[6px] -left-4 inline-block rounded-full group-hover:text-white",
      page.url.pathname === href
        ? "opacity-100"
        : "opacity-0 group-hover:opacity-5",
    ]}
    aria-hidden="true"
  ></span>
  <span class="relative">
    <a
      {href}
      class={[
        "text-2xl md:text-2xl md:font-bold",
        page.url.pathname === href
          ? "text-secondary-foreground"
          : "text-foreground",
      ]}>{label}</a
    >
  </span>
</li>
