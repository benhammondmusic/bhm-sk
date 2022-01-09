<script lang="ts">
	import { page } from '$app/stores';
</script>

<header>
	<div class="corner" />

	<nav class="main_nav">
		<ul class="d-flex flex-row align-items-start justify-content-start">
			<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Home</a></li>
			<li class:active={$page.path === '/shows'}><a sveltekit:prefetch href="/shows">Shows</a></li>
			<li class:active={$page.path === '/music'}><a sveltekit:prefetch href="/music">Music</a></li>
			<li class:active={$page.path === '/songlist'}>
				<a sveltekit:prefetch href="/songlist">Songlist</a>
			</li>
			<li class:active={$page.path === '/booking'}>
				<a sveltekit:prefetch href="/booking">Booking</a>
			</li>
			<li class:active={$page.path === '/contact'}>
				<a sveltekit:prefetch href="/contact">Contact</a>
			</li>
		</ul>
	</nav>

	<div class="corner" />
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}

	.corner {
		width: 3em;
		height: 3em;
	}

	nav {
		display: flex;
		justify-content: center;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li.active::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--accent-color);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--pure-white);
		font-weight: 400;
		font-size: 0.8rem;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--accent-color);
	}
</style>
