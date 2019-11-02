<script>
  import { Link } from "svelte-routing";
</script>

<style>
  nav {
    background: orange;
    display: grid;
    grid-template-columns: auto 1fr;
    padding: 10px 0;
  }
  ul {
    height: 30px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    list-style: none;
    margin: 0;
    align-items: center;
  }
</style>

<nav>
  <ul>
    <li>
      <Link to="/">Home</Link>
    </li>
  </ul>
</nav>
