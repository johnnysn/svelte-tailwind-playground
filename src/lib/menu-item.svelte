<script lang="ts">
	export let icon: ConstructorOfATypedSvelteComponent;
	export let label: string;
	export let showLabel: boolean;
	export let active = false;

	export let onClick: () => void;
</script>

<button
	class="flex items-center border border-transparent rounded transition-colors duration-150
  py-1 px-2 hover:bg-zinc-500 cursor-pointer h-8"
	on:click={onClick}
>
	<svelte:component this={icon} />
	<!-- {#if showLabel} -->
	<span class={`${showLabel ? 'w-28' : 'w-0'} overflow-hidden transition-all duration-300`}>{label}</span>
	<!-- {/if} -->
	<div class={`ml-1 w-2 h-2 rounded-full ${active ? 'bg-teal-400' : 'transparent'}`}></div>

</button>
