<script>
	import { songs } from '../data/songlist.json';
</script>

<svelte:head>
	<title>Song List</title>
</svelte:head>

<section>
	<h1>Song List</h1>

	<div class="songs">
		<!-- LOOP EVERY SONG -->
		{#each songs as song}
			<article class="songItem">
				<!-- EACH SONG'S TITLE -->
				{song.title} -
				<!-- EACH SONG'S ARTIST(S) -->
				{#each song.artistArray as artist, i}
					{artist}{i < song.artistArray.length - 1 ? ', ' : ''}
				{/each}
			</article>
		{/each}
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}

	.songs {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-evenly;
	}

	.songItem {
		margin: 10px;
		padding: 15px;
		background-color: #336699;
		border-radius: 5px;
		color: #ddeeff;
		font-weight: 400;
		font-size: 1.3rem;
	}
</style>
