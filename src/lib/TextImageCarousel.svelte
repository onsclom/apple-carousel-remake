<script lang="ts">
	export let items: { text: string; image: string }[];
	let index = 0;
	$: index = (index + items.length) % items.length;
</script>

<div class="space-y-5">
	<div class="flex items-center justify-center space-x-5">
		<button
			class="h-12 w-12 rounded-full bg-gray-200 text-lg hover:bg-gray-100"
			on:click={() => (index -= 1)}>←</button
		>
		<div class="flex max-w-xs flex-1 overflow-hidden rounded-3xl bg-gray-50">
			{#each items as item}
				<div
					class="flex w-full flex-shrink-0 flex-col justify-between overflow-hidden transition-transform duration-300"
					style:transform="translateX({-100 * index}%)"
				>
					<p class="flex justify-center px-4 py-14 text-center align-middle">
						{item.text}
					</p>
					<img src={item.image} alt={item.text} />
				</div>
			{/each}
		</div>
		<button
			class="h-12 w-12 rounded-full bg-gray-200 text-lg hover:bg-gray-100"
			on:click={() => (index += 1)}>→</button
		>
	</div>

	<div class="flex items-center justify-center">
		{#each items as _, i}
			<button class="group flex justify-center p-3 align-middle" on:click={() => (index = i)}>
				<div
					class="h-2 w-2 rounded-full bg-gray-300 transition-colors"
					class:bg-gray-500={i === index}
					class:group-hover:bg-gray-400={i !== index}
				></div>
			</button>
		{/each}
	</div>
</div>
