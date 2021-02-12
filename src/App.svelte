<script>
  import { Router, Link, Route } from "svelte-routing";

  import One from "./galleries/One.svelte";
  import Two from "./galleries/Two.svelte";
  import Three from "./galleries/Three.svelte";

  export let url = "";
</script>

<Router url="{url}">

	<Route path="/">
    <ul>
      <li>
        <Link to="one">Beispiel 1</Link>
      </li>
      <li>
        <Link to="two">Beispiel 2</Link>
      </li>
      <li>
        <Link to="three">Beispiel 3</Link>
      </li>
    </ul>
  </Route>
  <Route path="one" component={One} />
  <Route path="two" component={Two} />
  <Route path="three" component={Three} />

</Router>

<style lang="scss">

  ul {
    padding: 1rem;
  }

</style>
