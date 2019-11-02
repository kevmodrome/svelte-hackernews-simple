<script>
  export let id, title, points, user, time_ago, comments_count, url;

  import { Link } from "svelte-routing";
</script>

<style>
  article {
    padding: 5px 10px;
    margin: 15px;
    background: rgb(248, 248, 248);
    border-radius: 10px;
  }
</style>

<article>
  <h2>
    <a href={url}>{title}</a>
  </h2>
  <p>
    {points} points by {user} {time_ago}
    <Link to={`/item/${id}`}>{comments_count} comments</Link>
  </p>
</article>
