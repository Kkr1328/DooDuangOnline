<script>
    import Button, { Label }  from '@smui/button';

    let gifs = [];
    let searchTerm = "";

    async function searchForGif(e) {
        try {
        const returnValue = await fetch(`/giphy?term=${searchTerm}`);
        const response = await returnValue.json();
        gifs = response.data;
        } catch (error) {
        console.error(error);
        }
    }
</script>

<style>
  .gifs-grid {
    display: grid;
    grid-gap: 10px;
    grid-template-columns: repeat(5, 1fr);
  }
</style>

<div class="search-block">
    <input type="text" placeholder="Search for gif" bind:value={searchTerm} />
    <Button on:click={searchForGif}>Search</Button>
  </div>
  <div class="gifs">
    {#if gifs.length > 0}
      <div class="gifs-grid">
        {#each gifs as gif}
          <iframe src={gif.embed_url} title={gif.title} />
        {/each}
      </div>
    {:else}No gifs to show yet{/if}
  </div>