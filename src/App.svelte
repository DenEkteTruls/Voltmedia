<script>
	import router from "page";
	import Home from "./Home.svelte";
	import Loading from "./components/Loading.svelte";

	let page = Loading;

	router("/", () => page = Home);
	router("/loading", () => page = Loading);

	router.start();
</script>



<svelte:component this={page}/>