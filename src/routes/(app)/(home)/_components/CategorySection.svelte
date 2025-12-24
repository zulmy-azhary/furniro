<script lang="ts">
	import Section from '@/components/layout/section.svelte';
	import dining from '@/assets/images/category-dining.png';
	import living from '@/assets/images/category-living.png';
	import bedroom from '@/assets/images/category-bedroom.png';

	const categories = [
		{ image: dining, name: 'Dining' },
		{ image: living, name: 'Living' },
		{ image: bedroom, name: 'Bedroom' }
	];
</script>

<Section class="flex flex-col items-center gap-y-16">
	<div class="text-center">
		<h4 class="text-3xl font-bold text-slate-800">Browse The Range</h4>
		<p class="mt-2 text-lg text-slate-500">
			Lorem ipsum dolor sit amet, consectetur adipiscing elit.
		</p>
	</div>
	<div class="grid grid-cols-1 md:grid-cols-3 place-items-center w-full gap-6">
		{#each categories as category}
			<div class="flex flex-col items-center gap-y-8 w-full">
				<div class="w-full">
					<div class="overflow-hidden rounded-lg bg-slate-200 w-full h-96 md:h-80 lg:h-96 xl:h-128">
						<img
							src={category.image}
							alt={`${category.name}'s Photo`}
							class="size-full object-cover"
						/>
					</div>
				</div>
				<p class="text-xl font-semibold text-slate-700">{category.name}</p>
			</div>
		{/each}
	</div>
</Section>
