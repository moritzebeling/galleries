<script>
  import { Router, Link, Route } from "svelte-routing";

  import One from "./galleries/One.svelte";
  import Two from "./galleries/Two.svelte";
  import Three from "./galleries/Three.svelte";
  import Four from "./galleries/Four.svelte";
  import Five from "./galleries/Five.svelte";
  import Six from "./galleries/Six.svelte";

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
      <li>
        <Link to="four">Beispiel 4</Link>
      </li>
      <li>
        <Link to="five">Beispiel 5</Link>
      </li>
      <!-- <li>
        <Link to="six">Beispiel 6</Link>
      </li> -->
    </ul>
  </Route>

  <Route path="one" component={One} />
  <Route path="two" component={Two} />
  <Route path="three" component={Three} />
  <Route path="four" component={Four} />
  <Route path="five" component={Five} />
  <Route path="six" component={Six} />

</Router>

<style lang="scss">

  ul {
    padding: 1rem;
  }

</style>
