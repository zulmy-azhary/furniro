<script lang="ts">
	let { children } = $props();
</script>

<section class="px-4 2xl:px-24 flex justify-center w-full">
	<div class="container">
		{@render children()}
	</div>
</section>
