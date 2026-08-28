<script lang="ts">
  import type { Locale } from "$lib/Locale";
  import Footer from "../../../Footer.svelte";
  import Header from "../../../Header.svelte";

  let { locale }: { locale: Locale } = $props()

</script>

<Header locale={locale} />
<section>
  <div class="section-inner">
      <h1>Select Location</h1>
      <button>Hugo's Tech Lab</button>
  </div>
</section>
<Footer />
<style>
  section {
    min-height: 80vh;
  }

  .section-inner {
        border: 1px solid rgb(0, 36, 156);
  }
</style>
