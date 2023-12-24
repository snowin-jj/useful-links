<script lang="ts">
	type Variant = 'default' | 'outline';
	export let variant: Variant = 'default';
</script>

<button id={variant}>
	<slot />
</button>

<style scoped>
	button {
		all: unset;
		cursor: pointer;
		height: 4vh;
		padding-inline: 0.8rem;
		border-radius: 10px;
		transition: background-color 0.3s ease;
	}

	#default {
		background-color: hsl(var(--secondary));
		color: hsl(var(--primary));
	}

	#default:hover {
		background-color: hsla(var(--secondary), 0.9);
	}

	button:focus-visible {
		outline: 2px solid hsl(var(--secondary));
		outline-offset: 2px;
	}

	#outline {
		border: 2px solid hsl(var(--accent));
		color: hsl(var(--secondary));
	}

	#outline:hover {
		background-color: hsla(var(--accent), 1);
	}
</style>
