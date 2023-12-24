<script lang="ts">
	import FeaturedCollections from '@/components/app/FeaturedCollections.svelte';
	import CollectionRow from '@/components/app/CollectionRow.svelte';
	import { popularCollections, collectionsForyou } from '@/data/collection';
</script>

<main class="app-container">
	<FeaturedCollections />
	<CollectionRow rowTitle="Popular collections" collections={popularCollections} />
	<CollectionRow rowTitle="For you" collections={collectionsForyou} />
</main>

<style scoped>
	.app-container {
		margin-block: 2rem;
	}
</style>
