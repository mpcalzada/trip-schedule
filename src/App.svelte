<script>
	import Navbar from "./components/Navbar.svelte";
	import Scheduler from "./components/Scheduler.svelte";
</script>

<main>
	<Navbar />
	<Scheduler />
</main>

<style>

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
