<script lang="ts">
	import { cn } from '@/utils';
	import type { HTMLAttributes } from 'svelte/elements';

	type SectionProps = HTMLAttributes<HTMLElement> & {
		wrapperClassName?: SectionProps['class'],
	};

	let { class: className, children, ...props }: SectionProps = $props();
</script>

<section class={cn("px-4 2xl:px-24 flex justify-center w-full", props.wrapperClassName)} {...props}>
	<div class={cn("container", className)}>
		{@render children?.()}
	</div>
</section>
