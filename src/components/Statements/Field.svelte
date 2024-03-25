<script lang="ts">
	import { createEventDispatcher } from 'svelte';
	import { current_component } from 'svelte/internal';

	const dispatch = createEventDispatcher();
	let active = false;
	let value = 'test';

	function fieldInit(ref: HTMLElement) {
		ref.focus();
		return {
			destroy() {
				dispatch('confirm');
			}
		};
	}
	function handleKeypress(e: KeyboardEvent) {
		switch (e.key) {
			case 'Enter':
				active = true;
				break;
        case 'Left'
		}
	}

	function deactivate() {
		active = false;
	}
</script>

<td>
	{#if active}
		<input type="text" use:fieldInit bind:value on:blur={deactivate} />
	{:else}
		<span on:keypress={handleKeypress} tabindex="0">{value}</span>
	{/if}
</td>
