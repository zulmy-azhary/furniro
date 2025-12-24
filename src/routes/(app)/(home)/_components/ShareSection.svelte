<script lang="ts">
	import share1 from '@/assets/images/share-1.png';
	import share2 from '@/assets/images/share-2.png';
	import share3 from '@/assets/images/share-3.png';
	import share4 from '@/assets/images/share-4.png';
	import share5 from '@/assets/images/share-5.png';
	import share6 from '@/assets/images/share-6.png';
	import share7 from '@/assets/images/share-7.png';
	import share8 from '@/assets/images/share-8.png';
	import share9 from '@/assets/images/share-9.png';
</script>

<section class="flex flex-col w-full">
	<div class="text-center space-y-4">
		<p class="text-slate-500 font-medium">Share your setup with</p>
		<h4 class="text-4xl font-bold">#FuniroFurniture</h4>
	</div>

	<div class="flex flex-row justify-center items-center gap-5 w-full overflow-hidden">
		<div class="flex flex-col gap-5 items-center">
			<div class="flex gap-5 items-end">
				<div class="w-[280px] h-[440px] bg-gray-200 overflow-hidden">
					<img src={share1} alt="Gambar" class="gallery-img" />
				</div>
				<div class="w-[465px] h-[356px] bg-gray-200 overflow-hidden">
					<img src={share2} alt="Gambar" class="gallery-img" />
				</div>
			</div>

			<div class="flex gap-5">
				<div class="flex gap-5">
					<div class="w-[385px] h-96 bg-gray-200 overflow-hidden">
						<img src={share3} alt="Gambar" class="gallery-img" />
					</div>
					<div class="w-[360px] h-64 bg-gray-200 overflow-hidden">
						<img src={share4} alt="Gambar" class="gallery-img" />
					</div>
				</div>
			</div>
		</div>

		<div class="flex items-center">
			<div class="w-80 h-lg bg-gray-200 overflow-hidden shadow-md">
				<img src={share5} alt="Gambar" class="gallery-img" />
			</div>
		</div>

		<div class="flex flex-row gap-5 items-center">
			<div class="flex flex-col gap-5">
				<div class="flex items-end gap-5">
					<div class="w-80 h-[335px] bg-gray-200 overflow-hidden">
						<img src={share6} alt="Gambar" class="gallery-img" />
					</div>
					<div class="w-[425px] h-[433px] bg-gray-200 overflow-hidden">
						<img src={share7} alt="Gambar" class="gallery-img" />
					</div>
				</div>
				<div class="flex gap-5">
					<div class="w-48 h-md bg-gray-200 overflow-hidden">
						<img src={share8} alt="Gambar" class="gallery-img" />
					</div>
					<div class="w-72 h-56 bg-gray-200 overflow-hidden">
						<img src={share9} alt="Gambar" class="gallery-img" />
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
</style>
