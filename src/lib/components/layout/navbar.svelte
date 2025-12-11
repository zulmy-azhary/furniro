<script lang="ts">
	import logo from '@/assets/logo.svg';
	import { Button } from '@/components/ui/button';
</script>

<header class="sticky top-0 z-10 w-full bg-white flex items-center justify-between px-16 py-7">
	<div class="flex items-center gap-x-1">
		<img src={logo} alt="Furniro's Logo" />
		<h3 class="font-bold text-3xl font-[Montserrat]!">Furniro</h3>
	</div>
	<nav class="flex items-center gap-x-20 font-medium">
		<a href="/">Home</a>
		<a href="/shop">Shop</a>
		<a href="/about">About</a>
		<a href="/contact">Contact</a>
	</nav>
	<div class="flex items-center gap-x-6">
		<Button title="Account" size="icon" variant="ghost" class="p-2 size-fit">
			<span class="icon-[mdi--account-alert-outline] size-7"></span>
		</Button>
		<Button title="Search" size="icon" variant="ghost" class="p-2 size-fit">
			<span class="icon-[akar-icons--search] size-7"></span>
		</Button>
		<Button title="Wishlist" size="icon" variant="ghost" class="p-2 size-fit">
			<span class="icon-[akar-icons--heart] size-7"></span>
		</Button>
		<Button title="Shopping Cart" size="icon" variant="ghost" class="p-2 size-fit">
			<span class="icon-[ant-design--shopping-cart-outlined] size-7"></span>
		</Button>
	</div>
</header>
