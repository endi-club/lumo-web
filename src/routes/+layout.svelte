<script>
	import '../app.css';
	let { children } = $props();
    import "@fontsource/poppins";
</script>

<nav>
	<ul>
		<li>
			<a href="/" class="active">Etusivu</a>
			<div class="line"></div>
		</li>
		<li><a href="/">Minun Lumo</a></li>
	</ul>
</nav>

<main>
	{@render children()}
</main>

<style>
	nav {
		position: fixed;
		top: 1rem;
		left: 50%;
		transform: translateX(-50%);
	}

	nav ul {
		display: flex;
		gap: 2rem;

		background: hsla(var(--background), 0.6);
		border: 1px solid hsl(var(--border));
		border-radius: 9999px;
		padding-block: 0.75rem;
		padding-inline: 1.5rem;

		backdrop-filter: blur(10px);
	}

	nav ul li {
		position: relative;
		padding-bottom: 0.3rem;
	}

	nav ul li .line {
		position: absolute;
		bottom: 0;
		left: 0;
		right: 0;
		height: 2px;
		background: linear-gradient(
			90deg,
			transparent,
			hsl(var(--secondary)),
            transparent
		);
		border-radius: 9999px;
	}

	nav ul li a.active {
		color: hsl(var(--secondary));
		font-weight: bold;
	}

	main {
		margin-top: 8rem;
	}
</style>
