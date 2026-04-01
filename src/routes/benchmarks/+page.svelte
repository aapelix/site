<script lang="ts">
	import { resolve } from '$app/paths';

	const rootPath = resolve(`/`);
</script>

<section class="mt-5 flex justify-center">
	<div class="flex w-1/4 flex-col gap-3">
		<a
			class="w-fit border border-dashed px-6 py-2 text-lg font-bold duration-300 hover:border-solid hover:bg-[#292524]"
			href={rootPath}>Go back</a
		>
	</div>
</section>
