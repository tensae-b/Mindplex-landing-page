<script lang="ts">
	import { Application } from '@splinetool/runtime';
	import GlowingBtn from '$lib/ui/GlowingBtn.svelte';
	import { onMount } from 'svelte';

	let canvas: HTMLCanvasElement | null = null;
	onMount(() => {
		const app = new Application(canvas);
		app.load('https://prod.spline.design/VEuho3NWmFQK-bnv/scene.splinecode');
	});
</script>

<section class="flex flex-col-reverse items-center mt-3.5 md:flex-row">
	<div
		class="absolute bg-[url('/hero_ellipse.svg')] w-full h-[109%] bg-no-repeat right-0 top-[-17rem] max-w-[797px] z-[-1] hidden md:block"
	></div>
	<div
		class="absolute bg-[url('/hero_blurred.svg')] w-full h-[115%] bg-no-repeat right-[30%] top-10 max-w-[797px] z-[-1] hidden md:block"
	></div>
	<div class="w-full max-w-[745px] flex flex-col gap-3.5 mb-3.75 items-center md:items-baseline">
		<h1 class="font-bold text-xl leading-9 backdrop-blur-md md:text-5xl md:leading-tight">
			Blockchain-based <span class="text-[#49FFB3] md:block">Decentralized </span>
			Media Network
		</h1>
		<p class="text-white font-[Montserrat] text-xs md:text-base md:leading-5 max-w-md">
			Mindplex is a magazine and a social media platform providing a dynamic space for creators,
			influencers, and media enthusiasts to connect and collaborate.
		</p>
		<div
			class="flex items-center justify-center cursor-pointer transition-all ease-in-out duration-300 mt-10 max-w-sm"
		>
			<GlowingBtn
				href="https://magazine.mindplex.ai"
				text="Go to Mindplex Magazine"
				fontSize="23px"
			/>
			<img
				src="/hero_arrow.svg"
				alt="hero"
				class="hidden md:block transition-transform duration-300 hover:translate-x-2.5"
			/>
		</div>
	</div>
	<div class="w-full max-w-[270px] md:max-w-[715px]">
		<canvas id="canvas3d" class="w-full h-full" width="100%" height="100%" bind:this={canvas}
		></canvas>
	</div>
</section>
