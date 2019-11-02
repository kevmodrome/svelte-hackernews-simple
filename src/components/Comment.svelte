<script>
  export let comment;
</script>

<style>
  .container {
    margin-left: 25px;
    margin-top: 20px;
  }
  p {
    color: grey;
    font-size: 0.9em;
  }
  .html {
    border-bottom: 1px solid lightgrey;
  }
</style>

{#each comment.comments as comment}
  <div class="container">
    <p>{comment.user} {comment.time_ago}</p>
    <div class="html">
      {@html comment.content}
    </div>
    <svelte:self {comment} />
  </div>
{/each}
