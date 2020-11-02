<script>
	export let episode
</script>

<div class='episode'>
	<a href='{episode.image.original}'>
		<img src='{episode.image.medium}' alt='Image for {episode.name} episode'>
	</a>
	<h2>Title: {episode.name}</h2>	         
  <h3>Season: {episode.season}</h3>
  <h3>Episode: {episode.number}</h3>         
  <br /><h3>Summary</h3>
	<div class="summary">{@html episode.summary}</div>	
</div>

<style>
	.episode {
		margin: 1em 0;
		border: 1px solid #ccc;
		padding: 1em;
		overflow: auto;
		background-color: #f3f3f3; 
		border-radius: 5px;
	}	
	.summary {
		clear: left;
		font-size: 1.15em;
		line-height: 1.5;
	}
	h2, h3 {
		font-weight: 400;
		margin: 0.5em 0 0.5em 0;  
	}
	h2, h3 {  
  	font-family: helvetica, arial, sans-serif;
	}
	h2 {        
  	font-size: 1.75em;
	}  
	h3 {        
		font-size: 1.5em;
	}	      
	img {
		box-shadow: 0px 4px 6px #666;
		border-radius: 5px;
		float: left;
		margin: 0em 1em 1em 0;
		max-width: 100%;
	}      
</style>
