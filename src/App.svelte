<!-- ///////////////////////// 
///////// script ////////////
///////////////////////////// -->
<script>
	import { Route, Router } from "svelte-routing";
	import Detail from "./detail/Detail.svelte";
	import Library from "./library/Library.svelte";
	import Create from "./create/Create.svelte";
	import Comments from "./comments/Comments.svelte"

	export let url = "";
</script>

<!-- ///////////////////////// 
///////// display ///////////
///////////////////////////// -->
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
		<Route path="/comments/:id" let:params>
			<Comments id={params.id}/>
		</Route>
		
	</main>
</Router>

<!-- ///////////////////////// 
////////// style ////////////
///////////////////////////// -->
<style>
</style>
