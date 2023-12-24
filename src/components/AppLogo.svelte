<script lang="ts">
	import Logo from '@/components/ui/LogoIcon.svelte';

	export let isShort: boolean = true;
</script>

<a href="/">
	<div class="svg-wrapper">
		<Logo />
	</div>
	{#if !isShort}
		<h2>Useful Links</h2>
	{/if}
</a>

<style scoped>
	.svg-wrapper {
		width: 32px;
		height: 32px;
	}
</style>
