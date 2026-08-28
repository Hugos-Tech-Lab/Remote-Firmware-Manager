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
    background: radial-gradient(circle at top left, #fff7d0 0%, transparent 30%),
      radial-gradient(circle at top right, #fff8d5 0%, transparent 30%),
      radial-gradient(
        circle at bottom left,
        rgb(255, 244, 190) 0%,
        transparent 30%
      ),
      radial-gradient(circle at bottom right, #fff7d2 0%, transparent 30%),
      #fff9e0;
    font-weight: bold;
  }
</style>
