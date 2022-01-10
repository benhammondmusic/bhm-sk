<script lang="ts">
	import { page } from '$app/stores';
	import logo from '../header/logo.svg';
</script>

<header>
	<nav>
		<img class="logo" src={logo} alt="Ben Hammond Music Logo" />
		<ul>
			<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Home</a></li>
			<li class:active={$page.path === '/originals'}>
				<a sveltekit:prefetch href="/originals">Originals</a>
			</li>
			<li class:active={$page.path === '/covers'}>
				<a sveltekit:prefetch href="/covers">Covers</a>
			</li>
			<li class:active={$page.path === '/contact'}>
				<a sveltekit:prefetch href="/contact">Contact</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}

	.logo {
		height: 3rem;
		padding-top: 1rem;
	}

	nav {
		display: flex;
		justify-content: space-between;
		width: 100%;
		padding-inline: 3rem;
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
