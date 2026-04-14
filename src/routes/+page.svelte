<script lang="ts">
	import { resolve } from '$app/paths';

	const galleryPath = resolve(`/gallery`);
</script>

<main>
	<header class="mt-[50%] flex justify-center md:mt-[20%]">
		<div class="flex w-2/3 items-center justify-between lg:w-1/4">
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

	<section class="mt-10 flex justify-center md:mt-5">
		<div class="flex w-2/3 flex-col gap-3 lg:w-1/4">
			<a
				class="w-fit border border-dashed px-6 py-2 text-lg font-bold duration-300 hover:border-solid hover:bg-[#292524]"
				href={galleryPath}>Gallery</a
			>
		</div>
	</section>
</main>
