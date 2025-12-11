<script>
	import Section from '@/components/layout/section.svelte';
	import MetaTitle from '@/components/misc/meta-title.svelte';
	import logo from '@/assets/logo.svg';
	import { Breadcrumb, Item, Link, List, Separator } from '@/components/ui/breadcrumb';
</script>

<MetaTitle title="Shop" />

<section class="py-24 bg-slate-100 w-full -mx-4 2xl:-mx-24 flex flex-col items-center gap-y-2">
	<img src={logo} alt="Furniro's Logo" />
    <h2 class="text-5xl font-medium">Shop</h2>
	<Breadcrumb>
		<List>
			<Item>
				<Link href="/">Home</Link>
			</Item>
            <Separator />
			<Item>
				<Link href="/shop">Shop</Link>
			</Item>
		</List>
	</Breadcrumb>
</section>

<Section>
	<h2>Tes Shop</h2>
</Section>
