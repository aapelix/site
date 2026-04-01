<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	import { onNavigate } from '$app/navigation';

	onNavigate((navigation) => {
		if (!document.startViewTransition) return;

		return new Promise((resolve) => {
			document.startViewTransition(async () => {
				trigger();
				setTimeout(async () => {
					resolve();
					await navigation.complete;

					setTimeout(() => {
						trigger();
					}, 200);
				}, 200);
			});
		});
	});

	let { children } = $props();

	import svg from '$lib/assets/aaro.svg';

	import { fly } from 'svelte/transition';

	let open = $state(false);

	function trigger() {
		open = !open;
	}
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

{@render children()}

<footer class="absolute bottom-5 flex w-full justify-end px-5">
	<enhanced:img src={svg} class="h-10" />
</footer>

{#if open}
	<div
		class="overlay fixed top-0 h-screen w-screen bg-[#7dd3fc]"
		class:active={open}
		in:fly={{ x: -window.innerWidth, duration: 500, opacity: 1 }}
		out:fly={{ x: window.innerWidth, duration: 500, opacity: 1 }}
	></div>
{/if}

<style>
	.overlay {
		position: fixed;
		inset: 0;
		user-select: none;
	}
</style>
