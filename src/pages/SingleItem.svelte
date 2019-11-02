<script>
  import Comment from "../components/Comment.svelte";

  export let id;

  let promise = fetch(`http://node-hnapi.herokuapp.com/item/${id}`).then(res =>
    res.json()
  );
</script>

{#await promise}
  <h2>Loading...</h2>
{:then data}
  <h2>{data.title}</h2>
  <p>submitted by {data.user} {data.time_ago}</p>
  <Comment comment={data} />
{/await}
