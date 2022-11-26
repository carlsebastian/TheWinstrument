<script>
	import Instrument from "./components/Instrument.svelte"
</script>

<main>
	<h1>Självstyre 2022-12-08</h1>
	<Instrument/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #169bab;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>