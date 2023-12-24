<script lang="ts">
	import Button from '../ui/Button.svelte';
</script>

<div class="featured-card">
	<div class="featured-card_img">
		<img src="/images/reading-collection.png" alt="Books and coffee on the shevles" />
	</div>
	<div class="featured-card_content">
		<h1 class="card-title">Explore the new collection of Atomic books</h1>
		<p class="card-description">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus soluta magnam explicabo,
			laborum cupiditate aliquid. Dicta consequuntur veritatis neque sapiente.
		</p>
		<a href="/collections/1" class="featured-card_action">
			<Button variant="outline">View</Button>
		</a>
	</div>
</div>

<style scoped>
	.featured-card {
		padding: 1rem;
		display: flex;
		align-items: center;
		gap: 2rem;
		border: 2px solid hsl(var(--accent));
		border-radius: 10px;
	}

	.featured-card_img {
		width: 36rem;
		aspect-ratio: 1 / 1;
		overflow: hidden;
		border-radius: 10px;
	}

	.featured-card_content {
		display: flex;
		flex-direction: column;
		gap: 0.4rem;
	}

	.featured-card_action {
		width: fit-content;
	}
</style>
