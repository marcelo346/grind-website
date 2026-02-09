<script lang="ts">
	import { siteConfig } from '$lib/data/content';

	const pages = [
		'/images/project-visuals/page-00.webp',
		'/images/project-visuals/page-01.webp',
		'/images/project-visuals/page-02.webp'
	];
</script>

<svelte:head>
	<title>Project Visuals | {siteConfig.name}</title>
	<meta name="description" content="Visual overview of GRIND Collective projects and initiatives." />
	<meta property="og:title" content="Project Visuals | {siteConfig.name}" />
	<meta property="og:description" content="Visual overview of GRIND Collective projects and initiatives." />
</svelte:head>

<!-- Page Header -->
<section class="bg-off-white py-16 lg:py-24">
	<div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
		<div class="max-w-3xl">
			<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-urban-charcoal">
				Project Visuals
			</h1>
			<p class="mt-6 text-xl text-urban-charcoal/70">
				A visual overview of GRIND Collective's projects and initiatives.
			</p>
		</div>
	</div>
</section>

<!-- Images -->
<section class="bg-white py-16 lg:py-24 border-t border-dust-sand/20">
	<div class="mx-auto max-w-6xl px-4 sm:px-6 lg:px-8">
		<!-- First two images side by side -->
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
			<div class="card-hover rounded-2xl overflow-hidden shadow-lg">
				<img
					src={pages[0]}
					alt="Project visuals page 1"
					class="w-full h-auto"
					loading="eager"
				/>
			</div>
			<div class="card-hover rounded-2xl overflow-hidden shadow-lg">
				<img
					src={pages[1]}
					alt="Project visuals page 2"
					class="w-full h-auto"
					loading="eager"
				/>
			</div>
		</div>
		<!-- Third image centered -->
		<div class="flex justify-center">
			<div class="card-hover w-full md:w-1/2 rounded-2xl overflow-hidden shadow-lg">
				<img
					src={pages[2]}
					alt="Project visuals page 3"
					class="w-full h-auto"
					loading="lazy"
				/>
			</div>
		</div>
	</div>
</section>

<style>
	.card-hover {
		transition: transform 0.3s ease-out, box-shadow 0.3s ease-out;
	}
	.card-hover:hover {
		transform: scale(1.03) rotate(1deg);
		box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
	}
</style>
