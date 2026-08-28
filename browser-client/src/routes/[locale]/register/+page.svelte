<script lang="ts">
  import type { Locale } from "$lib/Locale";
  import Header from "../../../Header.svelte";

  let { locale }: { locale: Locale } = $props()

</script>

<Header locale={locale} />
<section>
  <div class="section-inner">
    {#key locale}
      <button>Register</button>
      <button>Sign in</button>
      <h1>Username</h1>
      <button>Hugo's Tech Lab</button>
      <h1>Select Device</h1>
      <button>Car1</button>
      <button>Car2</button>
      <h3>We support you with electronics, tools, and programming..</h3>
    {/key}
  </div>
</section>

<style>
  section {
    min-height: 80vh;
  }

  .section-inner {
        border: 1px solid rgb(0, 36, 156);
  }
</style>
