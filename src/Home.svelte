<script>
  export let name;
  
	import { Router, Link, Route } from "svelte-routing";
  import Navbar from "./navbar.svelte";
</script>

<Navbar/>
<main class="container pt-5">
  <div class="bg-light p-5 rounded">
    <h1>Hello {name}!</h1>
    <p class="lead">
      This Site is Powered by the API of <b>Iptv-org.github.io</b>
    </p>
    <Link
      class="btn btn-lg btn-primary"
      to="/Watch"
      role="button">See Available Channels</Link>
    <hr>
    <small>Developed By Dev.itsarun</small>
  </div>
</main>
