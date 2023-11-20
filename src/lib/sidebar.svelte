<script>
	import {
		Angry,
		Armchair,
		ArrowLeftFromLine,
		ArrowRightFromLine,
		BadgeDollarSign,
		Banana,
		Blocks
	} from 'lucide-svelte';
	import MenuItem from './menu-item.svelte';

	let sidebarOpen = false;
	let activeIndex = -1;

	function handleClick() {
		sidebarOpen = !sidebarOpen;
	}
</script>

<aside
	data-open={sidebarOpen}
	class="w-[60px] data-[open=true]:w-48 bg-zinc-700 py-4 px-1
          absolute left-0 top-0 h-screen z-50 ease-in-out duration-300"
>
	<div class="w-full flex flex-col items-center px-2">
		<div class="w-full flex justify-end mb-8">
			<button on:click={handleClick}>
				{#if sidebarOpen}
					<ArrowLeftFromLine />
				{:else}
					<ArrowRightFromLine />
				{/if}
			</button>
		</div>

		<ul class="flex flex-col gap-2">
			<li>
				<MenuItem
					icon={BadgeDollarSign}
					label={'Earn money'}
					showLabel={sidebarOpen}
					onClick={() => (activeIndex = 0)}
					active={activeIndex === 0}
				/>
			</li>
			<li>
				<MenuItem
					icon={Angry}
					label={'Be angry'}
					showLabel={sidebarOpen}
					onClick={() => (activeIndex = 1)}
					active={activeIndex === 1}
				/>
			</li>
			<li>
				<MenuItem
					icon={Blocks}
					label={'Throw boxes'}
					showLabel={sidebarOpen}
					onClick={() => (activeIndex = 2)}
					active={activeIndex === 2}
				/>
			</li>
			<li>
				<MenuItem
					icon={Banana}
					label={'Eat a banana'}
					showLabel={sidebarOpen}
					onClick={() => (activeIndex = 3)}
					active={activeIndex === 3}
				/>
			</li>
			<li>
				<MenuItem
					icon={Armchair}
					label={'Be a babysitter'}
					showLabel={sidebarOpen}
					onClick={() => (activeIndex = 4)}
					active={activeIndex === 4}
				/>
			</li>
		</ul>
	</div>
</aside>
