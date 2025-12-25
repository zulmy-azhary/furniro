<script lang="ts">
	import { Input } from '@/components/ui/input';
	import { Button } from '@/components/ui/button';

	const footers = [
		{
			title: 'Links',
			navs: [
				{ name: 'Home', href: '/' },
				{ name: 'Shop', href: '/shop' },
				{ name: 'About', href: '/about' },
				{ name: 'Contact', href: '/contact' }
			]
		},
		{
			title: 'Help',
			navs: [
				{ name: 'Payment Options', href: '/' },
				{ name: 'Returns', href: '/' },
				{ name: 'Privacy Policies', href: '/' }
			]
		}
	];
</script>

<footer class="border-t border-gray-300 flex flex-col items-center w-full px-4 2xl:px-24">
	<div class="container grid grid-cols-2 my-24 gap-y-[85px] md:grid-cols-4 xl:grid-cols-6 xl:my-12">
		<div class="flex flex-col col-span-full xl:col-span-2 gap-y-10">
			<div class="">
				<h3 class="font-[Montserrat] font-bold text-2xl">Furniro.</h3>
				<p class="font-light xl:max-w-xs text-gray-400">
					Furniro delivers modern, beautifully crafted furniture designed to elevate your living
					space with comfort and elegance.
				</p>
			</div>
			<div class="">
				<p class="font-light xl:max-w-xs text-sm">400 University Drive Suite 200 Coral Gables,</p>
				<p class="font-light xl:max-w-xs text-sm">FL 33134 USA</p>
				<p class="tracking-wide text-sm mt-1">cs@furniro.com</p>
			</div>
		</div>
		{#each footers as footer}
			<div class="space-y-14 md:col-span-1 lg:col-span-1">
				<h4 class="text-gray-400 tracking-wide font-medium">{footer.title}</h4>
				<ul class="flex flex-col gap-y-10">
					{#each footer.navs as nav}
						<a
							href={nav.href}
							class="tracking-tight hover:text-slate-400 md:tracking-wide font-medium"
						>
							{nav.name}
						</a>
					{/each}
				</ul>
			</div>
		{/each}

		<!-- Newsletter -->
		<div class="col-span-2 md:col-span-2 xl:col-span-2 space-y-14">
			<h4 class="text-gray-400 tracking-wide font-medium">Newsletter</h4>
			<div class="flex w-full max-w-sm items-center gap-2">
				<Input
					type="email"
					placeholder="Enter Your Email Address"
					class="tracking-wide px-3 py-1.5 rounded-none border-0 border-b border-input focus-visible:ring-0"
				/>
				<Button
					type="submit"
					variant="link"
					class="font-normal uppercase text-slate-700 font-[Poppins]"
				>
					Subscribe
				</Button>
			</div>
		</div>
	</div>
	<div
		class="container flex flex-col items-center justify-between py-6 border-t border-gray-300 gap-y-6 md:flex-row lg:py-9"
	>
		<p class="tracking-wide text-center md:text-start text-sm lg:text-base">
			Copyright © 2025 Furniro®. All rights reserved.
		</p>
	</div>
</footer>
