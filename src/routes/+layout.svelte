<script lang="ts">
	import '@/globals.css';
	import Footer from '@/components/Footer.svelte';
	import Header from '@/components/Header.svelte';
</script>

<section class="root-layout">
	<Header />
	<div class="main-container">
		<slot />
	</div>
	<Footer />
</section>

<style>
	.root-layout {
		max-width: 60rem;
		min-height: 100vh;
		min-height: 100svh;
		margin-inline: auto;
		padding-inline: 2rem;
		display: grid;
		grid-template-rows: auto 1fr auto;
	}
</style>
