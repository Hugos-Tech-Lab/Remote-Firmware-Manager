<script lang="ts">
  import type { Locale } from "$lib/Locale";
  import Logo from "./Logo.svelte";
  import Translations from "./Translations.svelte";

	let { locale }: { locale: Locale } = $props();
</script>

<header>
  <div class="section-inner">
    <Logo />
    <!-- <Translations {locale} /> -->
    <h1 class="title">
      Remote Firmware Manager
    </h1>
  </div>
</header>

<style>

  .title {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    top: 0;
    right: 0;
    text-align: right;
  }

  .section-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
</style>