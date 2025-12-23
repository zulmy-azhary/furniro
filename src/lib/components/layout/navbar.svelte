<script lang="ts">
	import logo from '@/assets/logo.svg';
	import { Button } from '@/components/ui/button';

	let isMenuOpen = false;

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}

	function closeMenu() {
		isMenuOpen = false;
	}
</script>

<header class="sticky top-0 z-20 w-full bg-white">
	<div class="flex items-center justify-between px-6 md:px-16 py-7">
		<div class="flex items-center gap-x-1">
			<img src={logo} alt="Furniro's Logo" />
			<h3 class="font-bold text-3xl font-[Montserrat]!">Furniro</h3>
		</div>

		<!-- Desktop Navigation -->
		<nav class="hidden lg:flex items-center gap-x-20 font-medium">
			<a href="/">Home</a>
			<a href="/shop">Shop</a>
			<a href="/about">About</a>
			<a href="/contact">Contact</a>
		</nav>

		<!-- Desktop Icons -->
		<div class="hidden lg:flex items-center gap-x-6">
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

		<!-- Hamburger Button (Mobile) -->
		<Button
			onclick={toggleMenu}
			title="Menu"
			size="icon"
			variant="ghost"
			class="lg:hidden p-2 size-fit relative z-50"
		>
			{#if isMenuOpen}
				<span class="icon-[mdi--close] size-7"></span>
			{:else}
				<span class="icon-[mdi--menu] size-7"></span>
			{/if}
		</Button>

		<!-- Mobile Menu -->
		{#if isMenuOpen}
			<aside class="lg:hidden fixed inset-0 bg-white pt-20 flex flex-col">
				<nav class="flex flex-col justify-evenly items-stretch text-center px-6 py-4 grow w-full">
					<a href="/" onclick={closeMenu} class="py-3 font-medium">Home</a>
					<a href="/shop" onclick={closeMenu} class="py-3 font-medium">Shop</a>
					<a href="/about" onclick={closeMenu} class="py-3 font-medium">About</a>
					<a href="/contact" onclick={closeMenu} class="py-3 font-medium">Contact</a>
				</nav>

				<div class="flex items-center justify-around px-6 py-4 border-t w-full">
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
			</aside>
		{/if}
	</div>
</header>
