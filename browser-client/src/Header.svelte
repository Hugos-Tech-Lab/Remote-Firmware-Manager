<script lang="ts">
  import type { Locale } from "$lib/Locale";
  import Logo from "./Logo.svelte";
  import Translations from "./Translations.svelte";

	let { locale }: { locale: Locale } = $props();
</script>

<header>
  <div class="section-inner">
    <Logo />
    <Translations {locale} />
  </div>
</header>

<style>
  header {
    min-height: 20vh;
  }
  
  .section-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
</style>