<script lang="ts">
	let number = 5;

	$: {
		console.log("You're just being reactive");
		console.log(number);
	}
</script>

<div class="flex flex-col gap-2">
	<h1
		class="text-6xl bg-gradient-to-r from-blue-400 to-emerald-400
  font-bold inline-block text-transparent bg-clip-text mb-4"
	>
		This is a Svelte Playground
	</h1>

	<h2 class="text-3xl tracking-wider mb-2">
		Be not <span class="text-rose-400">afraid</span>, my friend
	</h2>

	<p class="max-w-sm">
		Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aliquam consectetur impedit, suscipit
		illo quasi, eos corrupti amet alias quo quaerat provident ex! Ipsam dolore perferendis assumenda
		reiciendis. Fugit, inventore velit!
	</p>

	<p>Let's increment or decrement stuff</p>

	<h3 class="text-8xl">{number}</h3>

	<div class="flex items-center gap-4">
		<button
			class="bg-blue-500 hover:bg-blue-400 px-6 py-2 rounded transition-colors duration-300"
			on:click={() => number++}>Increment +</button
		>
		<button
			class="bg-rose-500 hover:bg-rose-400 px-6 py-2 rounded transition-colors duration-300"
			on:click={() => number--}>Decrement +</button
		>
	</div>
</div>
