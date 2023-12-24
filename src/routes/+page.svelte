<script lang="ts">
	import Button from '@/components/ui/Button.svelte';
</script>

<main class="site-container">
	<div class="content">
		<h1 class="title">
			Discover, Learn, Grow with <span class="keyword-block">Useful Links Hub</span>
		</h1>
		<p>
			Unlock a world of knowledge with Useful Links – Your go-to destination for learning,
			documentation, resources, and beyond. Explore, expand, and elevate your understanding
			effortlessly.
		</p>
		<a href="/explore">
			<Button>Explore</Button>
		</a>
	</div>
</main>

<style scoped>
	.site-container {
		height: 100%;
		display: grid;
		place-items: center;
	}

	.content {
		width: 100%;
		max-width: 38rem;
		height: 100%;
		margin-inline: auto;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 0.6rem;
		text-align: center;
	}

	.content .title {
		font-size: 2em;
		font-weight: 900;
		text-wrap: balance;
	}

	.title .keyword-block {
		color: hsl(var(--muted));
	}
</style>
