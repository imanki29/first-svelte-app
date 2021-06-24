<script>
	import { Route, Router } from "svelte-routing";
	import Detail from "./detail/Detail.svelte";
	import Library from "./library/Library.svelte";
	import Create from "./create/Create.svelte"

	export let url = "";
</script>

<Router {url}>
	<main>
		<Route path="/create">
			<Create />
		</Route>
		<Route path="/books/:id" let:params>
			<Detail id={params.id} />
		</Route>
		<Route path="/">
			<Library />
		</Route>
	</main>
</Router>

<style>
</style>
