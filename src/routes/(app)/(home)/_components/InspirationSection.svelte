<script lang="ts">
	import Section from '@/components/layout/section.svelte';
	import { Button } from '@/components/ui/button';
	import inspiration1 from '@/assets/images/inspiration-1.png';
	import inspiration2 from '@/assets/images/inspiration-2.png';
	import inspiration3 from '@/assets/images/inspiration-3.png';
</script>

<div class="w-full bg-amber-50/60 py-10">
	<Section wrapperClassName="pr-0!" class="flex items-center gap-6">
		<div class="basis-4/12 space-y-4">
			<h4 class="text-4xl font-bold">50+ Beautiful rooms inspiration</h4>
			<p class="text-slate-500 max-w-96">
				Our designer already made a lot of beautiful prototipe of rooms that inspire you
			</p>
			<Button variant="accent" size="md" class="px-6 md:px-8 mt-4">Explore More</Button>
		</div>
		<div class="basis-8/12 relative overflow-hidden">
			<div class="flex gap-x-6 w-fit">
				<div class="relative">
					<div class="bg-gray-200 h-128 w-96">
						<img src={inspiration1} alt="Inspiration Bed Room's" class="size-full object-cover" />
					</div>
					<div class="absolute z-0 left-6 bottom-6 flex items-end">
						<div class="bg-white/80 p-8 space-y-2">
							<p class="text-slate-700">01 - Bed Room</p>
							<h5 class="text-3xl font-semibold">Inner Peace</h5>
						</div>
						<Button variant="accent" size="icon-lg">
							<span class="icon-[ion--arrow-forward] size-6"></span>
						</Button>
					</div>
				</div>
				<div class="h-[420px] w-80">
					<img src={inspiration2} alt="Inspiration 2's" class="size-full object-cover" />
				</div>
				<div class="h-[420px] w-80">
					<img src={inspiration3} alt="Inspiration 3's" class="size-full object-cover" />
				</div>
			</div>

			<!-- Arrow -->
			<div
				class="absolute z-10 right-24 top-1/2 -translate-y-1/2 size-12 bg-white rounded-full shadow-lg flex items-center justify-center cursor-pointer hover:bg-slate-50"
			>
				<span class="icon-[akar-icons--chevron-right-small] size-6 text-yellow-700"></span>
			</div>

			<!-- Dots -->
			<div class="flex items-center gap-x-5 absolute z-10 bottom-8 left-[420px]">
				<div class="cursor-pointer p-1.5 border rounded-full border-yellow-700">
					<span class="block size-2.5 bg-yellow-700 rounded-full"></span>
				</div>
				<div class="cursor-pointer">
					<span class="block size-2.5 bg-gray-300 hover:bg-gray-400 rounded-full"></span>
				</div>
				<div class="cursor-pointer">
					<span class="block size-2.5 bg-gray-300 hover:bg-gray-400 rounded-full"></span>
				</div>
				<div class="cursor-pointer">
					<span class="block size-2.5 bg-gray-300 hover:bg-gray-400 rounded-full"></span>
				</div>
			</div>
		</div>
	</Section>
</div>
