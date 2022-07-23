<script>
	export let name;

	import { Router, Link, Route } from "svelte-routing";
	import Body from "./Home.svelte";
	import Watch from "./Watch.svelte";

	export let url = "";
</script>

<Router url="{url}">
	<main class="flex-shrink-0">
		<Route path="/"><Body name={name}/></Route>    
		<Route path="/Watch" component="{Watch}" location={Watch} />
	</main>
</Router>
