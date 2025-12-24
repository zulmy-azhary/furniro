<script lang="ts">
	import Section from '@/components/layout/section.svelte';
	import { Button } from '@/components/ui/button';
	import product1 from '@/assets/images/product-1.png';
	import product2 from '@/assets/images/product-2.png';
	import product3 from '@/assets/images/product-3.png';
	import product4 from '@/assets/images/product-4.png';
	import product5 from '@/assets/images/product-5.png';
	import product6 from '@/assets/images/product-6.png';
	import product7 from '@/assets/images/product-7.png';
	import product8 from '@/assets/images/product-8.png';

	const products = [
		{
			image: product1,
			name: 'Syltherine',
			description: 'Stylish cafe chair',
			price: 3500000,
			discount: 30
		},
		{
			image: product2,
			name: 'Leviosa',
			description: 'Stylish cafe chair',
			price: 2500000,
			discount: 0
		},
		{
			image: product3,
			name: 'Lolito',
			description: 'Luxury big sofa',
			price: 14000000,
			discount: 50
		},
		{
			image: product4,
			name: 'Respira',
			description: 'Outdoor bar table and stool',
			price: 500000,
			discount: 0
		},
		{
			image: product5,
			name: 'Grifo',
			description: 'Night lamp',
			price: 1500000,
			discount: 0
		},
		{
			image: product6,
			name: 'Muggo',
			description: 'Small mug',
			price: 150000,
			discount: 0
		},
		{
			image: product7,
			name: 'Pingky',
			description: 'Cude bed set',
			price: 14000000,
			discount: 50
		},
		{
			image: product8,
			name: 'Potty',
			description: 'Minimalist flower pot',
			price: 500000,
			discount: 0
		}
	];
</script>

<Section class="flex flex-col items-center gap-y-12">
	<h4 class="text-3xl font-bold text-slate-800">Our Products</h4>
	<div
		class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 place-items-center w-full gap-8"
	>
		{#each products as product}
			<div class="flex flex-col w-full bg-gray-100 relative">
				{#if product.discount > 0}
					<div
						class="absolute rounded-full size-14 top-4 right-4 bg-red-400 flex justify-center items-center"
					>
						<p class="text-white text-lg font-medium leading-none">
							-{product.discount}%
						</p>
					</div>
				{/if}
				<div class="w-full">
					<div class="w-full h-80 bg-slate-200 overflow-hidden">
						<img
							src={product.image}
							alt={`${product.name}'s Image`}
							class="size-full object-cover"
						/>
					</div>
				</div>
				<div class="px-4 py-6 space-y-2">
					<p class="text-2xl font-semibold text-slate-700">{product.name}</p>
					<p class="font-medium text-slate-400">{product.description}</p>
					<div class="flex items-center gap-x-4">
						<p class="text-lg font-semibold">
							{new Intl.NumberFormat('id-ID', {
								style: 'currency',
								currency: 'IDR',
								maximumFractionDigits: 0
							}).format(
								product.discount > 0
									? product.price - product.price * (product.discount / 100)
									: product.price
							)}
						</p>
						{#if product.discount > 0}
							<p class="line-through text-slate-400">
								{new Intl.NumberFormat('id-ID', {
									style: 'currency',
									currency: 'IDR',
									maximumFractionDigits: 0
								}).format(product.price)}
							</p>
						{/if}
					</div>
				</div>
			</div>
		{/each}
	</div>
	<Button variant="outline" size="md">Show More</Button>
</Section>
