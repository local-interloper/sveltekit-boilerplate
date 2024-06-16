<script lang="ts">
	import Svelte from '~icons/simple-icons/svelte';
	import Tailwind from '~icons/simple-icons/tailwindcss';
	import DaisyUi from '~icons/simple-icons/daisyui';
	import Iconify from '~icons/simple-icons/iconify';

	const plugins = [
		{ name: 'Svelte', Icon: Svelte },
		{ name: 'Tailwind', Icon: Tailwind },
		{ name: 'DaisyUi', Icon: DaisyUi },
		{ name: 'Iconify', Icon: Iconify }
	];
</script>

<section class="flex flex-col gap-5 justify-center items-center w-full h-full">
	<article>
		<span>local.interloper's</span>
		<h1 class="text-6xl">SvelteKit Template</h1>
	</article>
	<article class="flex flex-col gap-5 justify-center items-center">
		<span>Batteries included:</span>
		<article class="flex gap-2 items-center justify-center w-full">
			{#each plugins as { name, Icon }}
				<section class="tooltip tooltip-bottom" data-tip="{name}">
					<Icon class="bg-base-200 shadow text-6xl p-2 rounded" />
				</section>
			{/each}
		</article>
	</article>
</section>