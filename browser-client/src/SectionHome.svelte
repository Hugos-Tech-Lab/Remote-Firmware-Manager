<script lang="ts">
  import type { Locale } from "$lib/Locale";

  let { locale }: { locale: Locale } = $props()

</script>

<section>
  <div class="section-inner">
    {#key locale}
      <h1 id="intro" class="translation text-[clamp(48px,6vw,80px)]">FIX ANYTHING YOURSELF</h1>
      <h3 class="translation">We support you with electronics, tools, and programming..</h3>
    {/key}
  </div>
</section>

<style>
  section {
    min-height: 80vh;
  }
</style>
