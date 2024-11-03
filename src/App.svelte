<script lang="ts">
	import Card from './lib/card.svelte';

	const cards = new Array(10).fill(0).map((_, i) => ({
		name: `Card ${i + 1}`,
		cientificName: `Cientific name ${i + 1}`,
		origin: `Origin ${i + 1}`,
		src: `https://i0.wp.com/www.maispb.com.br/wp-content/uploads/2018/06/semente.jpg?fit=576%2C480&quality=90&strip=all&ssl=1`,
	}));
</script>

<header
	class="bg-white py-4 flex justify-center items-center border-b-2 shadow-md"
>
	<h1 class="text-2xl font-bold">Projeto Itapicuru</h1>
</header>
<main class="flex bg-#f0f0f0 min-h-[100svh] w-full wrap gap-1 py-2 px-2">
	{#each cards as card}
		<Card {...card} />
	{/each}
</main>

<style>
	header {
		display: flex;
	}
</style>
