<script lang="ts">
  import { type Locale } from "$lib/Locale";
  import App from "../../App.svelte";
  import type { PageData } from "./$types";

  let { data }: { data: PageData } = $props();
</script>

<App locale={data.locale as Locale} />

<style lang="postcss">
  @reference "tailwindcss";
  :global(html) {
    font-family: "Cousin", system-ui, sans-serif;
    color: #08060d;
    background: rgb(245, 249, 255);
    font-weight: bold;
  }
</style>
