<script lang="ts">
  import { goto } from "$app/navigation";
  import { type Locale } from "$lib/Locale";
  import Footer from "../../Footer.svelte";
  import Header from "../../Header.svelte";
  import type { PageData } from "./$types";

  let { data }: { data: PageData } = $props();
</script>

<Header locale={data.locale as Locale} />

<section>
  <div class="section-inner">
    <button onclick={() => goto("/register")}>Register</button>
    <button>Sign in</button>
    <h1>Select Location</h1>
    <button>Hugo's Tech Lab</button>
    <h1>Select Device</h1>
    <button>Car1</button>
    <button>Car2</button>
    <h3>We support you with electronics, tools, and programming..</h3>
  </div>
</section>

<Footer />

<style lang="postcss">
  @reference "tailwindcss";
  :global(html) {
    font-family: "Cousin", system-ui, sans-serif;
    color: #08060d;
    background: rgb(245, 249, 255);
    font-weight: bold;
  }

  section {
    min-height: 80vh;
  }

  .section-inner {
    border: 1px solid rgb(0, 36, 156);
  }
</style>
