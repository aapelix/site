<script lang="ts">
	import { resolve } from '$app/paths';

	const galleryPath = resolve(`/gallery`);
	const benchmarksPath = resolve(`/benchmarks`);
</script>

<main>
	<header class="mt-[20%] flex justify-center">
		<div class="flex w-1/4 justify-between">
			<div>
				<h1 class="text-xl font-bold">aapelix.dev</h1>
				<p>aaro</p>
			</div>
			<a href="https://github.com/aapelix" target="_blank" aria-label="Github"
				><img
					alt="Github Logo"
					src="https://devicons.railway.com/i/github-light.svg"
					class="h-8 w-8"
				/></a
			>
		</div>
	</header>

	<section class="mt-5 flex justify-center">
		<div class="flex w-1/4 flex-col gap-3">
			<a
				class="w-fit border border-dashed px-6 py-2 text-lg font-bold duration-300 hover:border-solid hover:bg-[#292524]"
				href={galleryPath}>Gallery</a
			>
			<a
				class="w-fit border border-dashed px-6 py-2 text-lg font-bold duration-300 hover:border-solid hover:bg-[#292524]"
				href={benchmarksPath}>Benchmarks</a
			>
		</div>
	</section>
</main>
