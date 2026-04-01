<script lang="ts">
	import { resolve } from '$app/paths';

	const rootPath = resolve(`/`);

	const projects = [
		{
			name: 'aromi',
			link: 'https://github.com/aapelix/aromi'
		},
		{
			name: 'bg',
			link: 'https://github.com/aapelix/bg'
		},
		{
			name: 'wrum',
			link: 'https://github.com/aapelix/wrum'
		},
		{
			name: 'voi',
			link: 'https://github.com/aapelix/voi'
		}
	];
</script>

<section class="mt-5 flex justify-center">
	<div class="flex w-1/4">
		<a
			class="w-fit border border-dashed px-6 py-2 text-lg font-bold duration-300 hover:border-solid hover:bg-[#292524]"
			href={rootPath}>Go back</a
		>
	</div>
</section>

<section class="mt-[18%] flex justify-center">
	<div class="flex w-1/4 flex-col gap-3">
		{#each projects as project (project.link)}
			<a href={project.link} rel="external" class="group relative inline-block">
				{project.name}
				<span
					class="absolute -bottom-0.5 left-0 h-0.5 w-full origin-right scale-x-0 bg-white transition-transform duration-300 group-hover:origin-left group-hover:scale-x-100"
				></span>
			</a>
		{/each}
	</div>
</section>
