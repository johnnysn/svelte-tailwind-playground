<script lang="ts">
	export let icon: ConstructorOfATypedSvelteComponent;
	export let label: string;
	export let showLabel: boolean;
</script>

<div
	class="flex items-center gap-2 border border-transparent rounded transition-colors duration-150
  py-1 px-2 hover:border-zinc-200 cursor-pointer"
>
	<svelte:component this={icon} />
	{#if showLabel}
		<span>{label}</span>
	{/if}
</div>
