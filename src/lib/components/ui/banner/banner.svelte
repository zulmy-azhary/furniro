<script lang="ts">
	import logo from '@/assets/logo.svg';
	import banner from '@/assets/images/banner.png';
	import { Breadcrumb, Item, Link, List, Separator } from '@/components/ui/breadcrumb';

	type BannerProps = {
		image?: string;
		title: {
			name: string;
			path: string;
		};
	};

	let { image, title }: BannerProps = $props();
</script>

<section class="relative py-24 w-full -mx-4 2xl:-mx-24 flex flex-col items-center gap-y-2">
	<div class="absolute inset-0 -z-10">
		<img src={image ?? banner} alt="Banner" class="object-cover size-full opacity-50" />
	</div>
	<img src={logo} alt="Furniro's Logo" />
	<h2 class="text-5xl font-medium">{title.name}</h2>
	<Breadcrumb>
		<List>
			<Item>
				<Link href="/" class="font-medium">Home</Link>
			</Item>
			<Separator />
			<Item>
				<Link href={title.path}>{title.name}</Link>
			</Item>
		</List>
	</Breadcrumb>
</section>
