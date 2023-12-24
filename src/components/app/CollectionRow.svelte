<script lang="ts">
	import type { Collection } from '@/lib/types';
	import Button from '../ui/Button.svelte';

	export let collections: Collection[];
	export let rowTitle: string;
</script>

<section class="collection-wrapper">
	<h2>{rowTitle}</h2>
	<div class="popular-collections_wrapper">
		{#each collections as collection}
			<div class="popular-card">
				<div class="popular-card_img">
					<img src={collection.image} alt={collection.title} />
				</div>
				<div class="popular-card_content">
					<h3 class="card-title">{collection.title}</h3>
					<a href={`/collections/${collection.id}`} class="popular-card_action">
						<Button variant="outline">View</Button>
					</a>
				</div>
			</div>
		{/each}
	</div>
</section>

<style scoped>
	.collection-wrapper {
		margin-block: 2rem;
	}

	.popular-collections_wrapper {
		margin-block: 1rem;
		display: flex;
		flex-wrap: wrap;
		align-items: stretch;
		justify-content: center;
		gap: 0.8rem;
	}

	.popular-card {
		max-width: 18rem;
		padding: 1rem;
		flex: 1;
		align-self: normal;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: last baseline;
		gap: 2rem;
		border: 2px solid hsl(var(--accent));
		border-radius: 10px;
	}

	.popular-card_img {
		overflow: hidden;
		border-radius: 10px;
	}

	.popular-card_img img {
		aspect-ratio: 1 / 1;
		height: 100%;
	}

	.popular-card_content {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		gap: 0.4rem;
		margin-top: auto;
	}
	.card-title {
		font-size: 1em;
	}

	.popular-card_action {
		width: fit-content;
	}
</style>
