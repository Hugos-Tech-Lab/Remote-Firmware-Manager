<script lang="ts">
  import type { Locale } from "$lib/Locale";
  import { loadLocale } from 'wuchale/load-utils'
  import { goto } from "$app/navigation";

	let { locale }: { locale: Locale } = $props();

	async function changeLocale(newLocale: Locale) {
		if (newLocale === locale) return;

		await loadLocale(newLocale);

		const url = new URL(window.location.href);
		url.pathname = `/${newLocale}${url.pathname.replace(/^\/(eng|cze|ukr)/, '')}`;

		await goto(url);
	}
</script>

<div>
  <button class:active={locale === "eng"} onclick={() => changeLocale("eng")}>ENG</button>
  <button class:active={locale === "cze"} onclick={() => changeLocale("cze")}>CZE</button>
  <button class:active={locale === "ukr"} onclick={() => changeLocale('ukr')}>UKR</button>
</div>

<style>
  div {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    top: 0;
    right: 0;
  }

  button {
    width: fit-content;
    background: #fff9e0;
    border: 2px solid rgb(0, 0, 0);
    color: black;
    padding: 6px;
    border-radius: 1px;
    font: inherit;
    font-weight: bolder;
    cursor: pointer;
    margin: 5px;
    font-size: 12px;
    opacity: 0.5;
  }

  button.active {
    opacity: 1;
    background: #252283;
    color: #fff9e0;
  }
</style>
