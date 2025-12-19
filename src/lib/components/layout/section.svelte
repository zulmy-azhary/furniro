<script lang="ts">
	import { cn } from '@/utils';
	import type { HTMLAttributes } from 'svelte/elements';

	type SectionProps = HTMLAttributes<HTMLElement>;

	let { class: className, children, ...props }: SectionProps = $props();
</script>

<section class={cn("px-4 2xl:px-24 flex justify-center w-full", className)} {...props}>
	<div class="container">
		{@render children?.()}
	</div>
</section>
