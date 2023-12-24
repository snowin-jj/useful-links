<script>
	import AppLogo from '@/components/AppLogo.svelte';
	import Button from '@/components/ui/Button.svelte';
</script>

<header class="site-header">
	<AppLogo />
	<nav>
		<a href="/about">About</a>
		<a href="/collections">Collections</a>
		<Button>Sign In</Button>
	</nav>
</header>

<style>
	.site-header {
		height: 10vh;
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 1rem;
		font-size: 1em;
	}

	.site-header nav {
		display: flex;
		align-items: center;
		gap: 2rem;
	}

	.site-header nav a:hover {
		transition: color 0.3s ease;
		color: hsl(var(--muted));
	}
</style>
