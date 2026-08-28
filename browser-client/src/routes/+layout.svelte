<script lang="ts">
	import '../app.css';
	import cousinFont from '../assets/fonts/Cousin-Bold.woff2';

	let { children } = $props();
</script>

<svelte:head>
	<link
		rel="preload"
		as="font"
		href={cousinFont}
		type="font/woff2"
		crossorigin="anonymous"
	/>
</svelte:head>

{@render children()}
