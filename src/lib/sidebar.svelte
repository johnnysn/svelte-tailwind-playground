<script>
	import { Angry, Armchair, ArrowLeftFromLine, ArrowRightFromLine, BadgeDollarSign, Banana, Blocks } from 'lucide-svelte';
	import MenuItem from './menu-item.svelte';

	let sidebarOpen = true;

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
        <MenuItem icon={BadgeDollarSign} label={'Earn money'} showLabel={sidebarOpen} />
      </li>
      <li>
        <MenuItem icon={Angry} label={'Be angry'} showLabel={sidebarOpen} />
      </li>
      <li>
        <MenuItem icon={Blocks} label={'Throw boxes'} showLabel={sidebarOpen} />
      </li>
      <li>
        <MenuItem icon={Banana} label={'Eat a banana'} showLabel={sidebarOpen} />
      </li>
      <li>
        <MenuItem icon={Armchair} label={'Be a babysitter'} showLabel={sidebarOpen} />
      </li>
    </ul>
	</div>
</aside>
