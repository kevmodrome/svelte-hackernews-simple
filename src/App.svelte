<script>
  import { Router, Route } from "svelte-routing";

  import Navigation from "./components/Navigation.svelte";
  import Home from "./pages/Home.svelte";
  import SingleItem from "./pages/SingleItem.svelte";
</script>

<style>
  div {
    max-width: 700px;
    margin: 0 auto;
  }
</style>

<Router>
  <Navigation />
  <div>
    <Route path="/item/:id" component={SingleItem} />
    <Route path="/" component={Home} />
  </div>
</Router>
