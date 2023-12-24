<script lang="ts">
	import '@/globals.css';
	import Footer from '@/components/Footer.svelte';
	import Header from '@/components/Header.svelte';
	import MaintainceImg from '@/assets/images/website-maintenance.png';

	const isProd = process.env.NODE_ENV === 'production';
</script>

{#if isProd}
	<section class="info-wrapper">
		<div class="info-container">
			<img src={MaintainceImg} alt="Men working on a site" />
			<h2>Working in progress</h2>
			<p>Please back come later :)</p>
		</div>
	</section>
{:else}
	<section class="root-layout">
		<Header />
		<div class="main-container">
			<slot />
		</div>
		<Footer />
	</section>
{/if}

<style scoped>
	.root-layout {
		max-width: 60rem;
		min-height: 100vh;
		min-height: 100svh;
		margin-inline: auto;
		padding-inline: 2rem;
		display: grid;
		grid-template-rows: auto 1fr auto;
	}

	.info-wrapper {
		min-height: 100vh;
		min-height: 100svh;
		display: grid;
		place-items: center;
		background-color: #ffffff;
		color: #404252;
		text-align: center;
	}

	.info-container img {
		width: 400px;
		aspect-ratio: 1 / 1;
		overflow: hidden;
	}

	.info-wrapper p {
	}
</style>
