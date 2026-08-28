<script lang="ts">
  import Header from "./Header.svelte";
  import SectionHome from "./SectionHome.svelte";
  import type { Locale } from "$lib/Locale";

  let { locale }: { locale: Locale } = $props();
</script>

<Header {locale} />
<div id="content">
  <SectionHome {locale} />
</div>

<footer>
  <div class="section-inner">© {new Date().getFullYear()} Hugo Luccarini. All Rights Reserved. Czech Business Number (IČO): 29876834. Icons made by <a href="https://flaticon.com/authors/design-circle" title="Author: Design Circle">Design Circle</a> and <a href="https://flaticon.com/authors/uniconlabs" title="Author: Uniconlabs">Uniconlabs</a> from  <a href="https://flaticon.com" title="Flaticon Website">flaticon.com</a></div>
</footer>
