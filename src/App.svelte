<script>
	import { onMount } from 'svelte'	
	import Episodes from './Episodes.svelte'
	const API_URL = 'http://api.tvmaze.com/singlesearch/shows?q=bosch&embed=episodes'
	let episodes = [];
	onMount(async () => {
		const resp = await fetch(API_URL)
		const json = await resp.json()
		episodes = await Array.from(json._embedded.episodes) 
	})
	
</script>

{#if episodes.length !== 0}
	<Episodes {episodes} />
{:else}
	Loading...
{/if}

