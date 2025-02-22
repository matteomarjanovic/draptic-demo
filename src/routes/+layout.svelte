<script lang="ts">
	import "../app.css";
	let { children } = $props();
</script>

<svelte:head>
	<script
		defer
		src="https://mm-umami.netlify.app/script.js"
		data-website-id="b80ba154-c32c-47aa-b133-6ab977537dbf"
	></script>
</svelte:head>

{@render children()}
