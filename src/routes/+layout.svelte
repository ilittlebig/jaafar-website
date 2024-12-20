<script lang="ts">
	import Navbar from "$lib/components/navbar.svelte";
	import "../app.css";
	let { children } = $props();
</script>

<Navbar />
<div class="mx-auto max-w-6xl">
	{@render children()}
</div>
