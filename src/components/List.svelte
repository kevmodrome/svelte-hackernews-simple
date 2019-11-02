<script>
  import Item from "./Item.svelte";

  export let route, page;

  let promise = fetch(`${route}${page}`).then(res => res.json());
</script>

{#await promise}
  <h2>Loading...</h2>
{:then data}
  {#each data as headline}
    <Item {...headline} />
  {/each}
{/await}
