<script lang="ts">
	import Table from './Table.svelte';
</script>

<section>
	<h2>Statements</h2>
	<Table />
</section>

<style>
	section {
		grid-area: statements;

		background-color: hsla(0, 0%, 0%, 0.2);
		border-radius: 1rem;
	}
</style>
