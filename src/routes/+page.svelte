<script lang="ts">
	import TextImageCarousel from '$lib/TextImageCarousel.svelte';

	const items = [
		{
			text: 'Three versatile options to best suit your studio.',
			image:
				'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/stand-mount-gallery-1-202203?wid=640&hei=528&fmt=p-jpg&qlt=95&.v=1645726292730'
		},
		{
			text: 'Tilt-adjustable stand offers 30 degrees of tilt.',
			image:
				'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/stand-mount-gallery-2-202203?wid=640&hei=528&fmt=p-jpg&qlt=95&.v=1645726292642'
		},
		{
			text: 'Tilt- and height-adjustable stand option adds 105 mm of height adjustability.',
			image:
				'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/stand-mount-gallery-3-202203?wid=640&hei=528&fmt=p-jpg&qlt=95&.v=1645726292791'
		},
		{
			text: `VESA mount adapter option attaches to a wall or desk mount, stand, or articulating arm and supports landscape and portrait orientation.`,
			image:
				'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/stand-mount-gallery-4-202203?wid=640&hei=528&fmt=p-jpg&qlt=95&.v=1645726292947'
		}
	];
</script>

<main class="pt-10">
	<TextImageCarousel {items} />
</main>
