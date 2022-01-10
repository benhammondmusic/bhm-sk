<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';

	const displayYear = new Date().getFullYear();
</script>

<Header />

<main>
	<slot />
</main>

<footer>
	<p>
		Site by <a href="https://benhammond.tech">benhammond.tech</a>
		<span class="copyright"> &copy; {displayYear}</span>
	</p>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a,
	footer p {
		font-weight: 400;
		color: var(--pure-white);
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
