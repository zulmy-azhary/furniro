<script lang="ts">
	import bgHero from '@/assets/images/bg-hero.png';
	import { Button } from '@/components/ui/button';
</script>

<section class="relative py-16 md:py-24 lg:py-40 w-full -mx-4 2xl:-mx-24 flex justify-end">
	<img
		src={bgHero}
		alt="Hero Background"
		class="absolute w-full h-full -z-10 inset-y-0 object-cover"
	/>
	<div class="px-4 2xl:px-16 flex justify-end w-full">
		<div
			class="w-full md:w-3/4 lg:w-1/2 p-8 md:p-12 bg-orange-100 rounded-md self-end flex flex-col gap-y-10"
		>
			<div class="flex flex-col">
				<p class="font-semibold tracking-widest mb-2 text-sm md:text-base">New Arrival</p>
				<h1 class="text-4xl md:text-5xl font-bold text-yellow-700 leading-tight mb-3 lg:max-w-sm">
					Discover Our New Collection
				</h1>
				<p class="font-normal tracking-wide text-base md:text-lg md:leading-tight lg:max-w-xl">
					Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut elit tellus, luctus nec
					ullamcorper mattis.
				</p>
			</div>
			<Button variant="accent" class="uppercase w-fit self-center md:self-start" size="lg">
				Buy Now
			</Button>
		</div>
	</div>
</section>
