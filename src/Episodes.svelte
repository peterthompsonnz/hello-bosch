<script>
	import Episode from './Episode.svelte'
	export let episodes
</script>

<header>
		<h1 class="title">
		Bosch Episodes
		</h1>
</header>
<main>	
	{#each episodes as episode (episode.id)}
		<Episode {episode} />
	{/each}	
</main>

<style>
	:global(body) {
		height: 100%;
		margin: 0;
		padding: 0;	
		font-size: 100%;
	}
	:global(main) {		
		margin: 0 auto;
		padding: 0.5em 1em;
		max-width: 768px;	
		background-color: #fff;
	}
	h1.title {       
		font-family: georgia, 'times new roman', times, serif; 
		font-size: 3.5em;
		letter-spacing: 0.01em;
		font-weight: 400;
		text-transform: uppercase;
		padding: 0.5em 0;
		color: #fff;
		text-align: center;        
		margin-top: 0;
	}
	header {
		background-color: #222;   
		margin-bottom: 2em; 
	}  
</style>