<script lang="ts">
	import Statements from '../components/Statements/Statements.svelte';
	import YearlyOverview from '../components/YearlyOverview/YearlyOverview.svelte';
</script>

<main>
	<Statements />
	<YearlyOverview />
</main>

<style>
	main {
		display: grid;
		grid-template-areas: 'yearly-overview yearly-overview statements';
	}
</style>
