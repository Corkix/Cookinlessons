<script lang="ts">
	import { TabGroup, Tab } from '@skeletonlabs/skeleton';
	import Footer from '$lib/components/Footer.svelte';

	let elemCarousel: HTMLDivElement;

	// Bilder som visas i karusellerna
	const solnedgångKarusellIds = [
		'https://hagablanket.se/wp-content/uploads/2021/05/skogslugnet1.jpg',
		'https://hagablanket.se/bilder/skogslugnet2',
		'https://hagablanket.se/bilder/skogslugnet3',
		'https://hagablanket.se/bilder/skogslugnet4',
		'https://hagablanket.se/bilder/skogslugnet5',
		'https://hagablanket.se/bilder/skogslugnet6'
	];
	const trädgårdKarusellIds = [
		'https://hagablanket.se/wp-content/uploads/2021/05/skogslugnet1.jpg',
		'https://hagablanket.se/bilder/skogslugnet2',
		'https://hagablanket.se/bilder/skogslugnet3',
		'https://hagablanket.se/bilder/skogslugnet4',
		'https://hagablanket.se/bilder/skogslugnet5',
		'https://hagablanket.se/bilder/skogslugnet6'
	];
	const inredningKarusellIds = [
		'https://hagablanket.se/wp-content/uploads/2021/05/skogslugnet1.jpg',
		'https://hagablanket.se/bilder/skogslugnet2',
		'https://hagablanket.se/bilder/skogslugnet3',
		'https://hagablanket.se/bilder/skogslugnet4',
		'https://hagablanket.se/bilder/skogslugnet5',
		'https://hagablanket.se/bilder/skogslugnet6'
	];
	const tänkvärtKarusellIds = [
		'https://hagablanket.se/wp-content/uploads/2021/05/skogslugnet1.jpg',
		'https://hagablanket.se/bilder/skogslugnet2',
		'https://hagablanket.se/bilder/skogslugnet3',
		'https://hagablanket.se/bilder/skogslugnet4',
		'https://hagablanket.se/bilder/skogslugnet5',
		'https://hagablanket.se/bilder/skogslugnet6'
	];

	// Bilder som visas i bild gallerierna
	const solnedgångIds = [
		'https://hagablanket.se/bilder/skogslugnet7',
		'https://hagablanket.se/bilder/skogslugnet8',
		'https://hagablanket.se/bilder/skogslugnet9',
		'https://hagablanket.se/bilder/skogslugnet10',
		'https://hagablanket.se/bilder/skogslugnet11',
		'https://hagablanket.se/bilder/skogslugnet12',
		'https://hagablanket.se/bilder/skogslugnet13',
		'https://hagablanket.se/bilder/skogslugnet14',
		'https://hagablanket.se/bilder/skogslugnet15',
		'https://hagablanket.se/bilder/skogslugnet16',
		'https://hagablanket.se/bilder/skogslugnet18',
		'https://hagablanket.se/bilder/skogslugnet19'
	];
	const trädgårdIds = [
		'https://hagablanket.se/bilder/skogslugnet7',
		'https://hagablanket.se/bilder/skogslugnet8',
		'https://hagablanket.se/bilder/skogslugnet9',
		'https://hagablanket.se/bilder/skogslugnet10',
		'https://hagablanket.se/bilder/skogslugnet11',
		'https://hagablanket.se/bilder/skogslugnet12',
		'https://hagablanket.se/bilder/skogslugnet13',
		'https://hagablanket.se/bilder/skogslugnet14',
		'https://hagablanket.se/bilder/skogslugnet15',
		'https://hagablanket.se/bilder/skogslugnet16',
		'https://hagablanket.se/bilder/skogslugnet18',
		'https://hagablanket.se/bilder/skogslugnet19'
	];
	const inredningIds = [
		'https://hagablanket.se/bilder/skogslugnet7',
		'https://hagablanket.se/bilder/skogslugnet8',
		'https://hagablanket.se/bilder/skogslugnet9',
		'https://hagablanket.se/bilder/skogslugnet10',
		'https://hagablanket.se/bilder/skogslugnet11',
		'https://hagablanket.se/bilder/skogslugnet12',
		'https://hagablanket.se/bilder/skogslugnet13',
		'https://hagablanket.se/bilder/skogslugnet14',
		'https://hagablanket.se/bilder/skogslugnet15',
		'https://hagablanket.se/bilder/skogslugnet16',
		'https://hagablanket.se/bilder/skogslugnet18',
		'https://hagablanket.se/bilder/skogslugnet19'
	];
	const tänkvärtIds = [
		'https://hagablanket.se/bilder/skogslugnet7',
		'https://hagablanket.se/bilder/skogslugnet8',
		'https://hagablanket.se/bilder/skogslugnet9',
		'https://hagablanket.se/bilder/skogslugnet10',
		'https://hagablanket.se/bilder/skogslugnet11',
		'https://hagablanket.se/bilder/skogslugnet12',
		'https://hagablanket.se/bilder/skogslugnet13',
		'https://hagablanket.se/bilder/skogslugnet14',
		'https://hagablanket.se/bilder/skogslugnet15',
		'https://hagablanket.se/bilder/skogslugnet16',
		'https://hagablanket.se/bilder/skogslugnet18',
		'https://hagablanket.se/bilder/skogslugnet19'
	];

	function carouselThumbnail(index: number) {
		elemCarousel.scroll(elemCarousel.clientWidth * index, 0);
	}

	let tabSet: number = 0;
</script>

<!-- <ol class="breadcrumb">
	<li class="crumb">Home</li>
	<li class="crumb-separator" aria-hidden>/</li>
</ol>
 -->

<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Hagablänket</title>
	</head>
	<body class="flex flex-col">
		<div class="gap-2">
			<section class="bg-gray-50">
				<div class="">
					<img
						alt=""
						src="https://hagablanket.se/wp-content/uploads/2022/12/Sidhuvud-Hagablankets-Undersidor.jpg"
						class="w-full h-full"
					/>
				</div>
			</section>
			<div class="flex p-2 lg:items-center lg:justify-between">
				<div class="flex-1">
					<section class="p-4 flex-row">
						<div class="card p-4 px-10">
							<article class="space-y-4">
								<h1 class="text-3xl font-bold sm:text-4xl">Njutbart</h1>
								<p>
									Här kan du stanna en stund och bara njuta av vackra bilder och ord under de olika
									flikarna. En hemsida kan fyllas enbart av fakta och viktig information men den kan
									också erbjuda en välbehövlig paus med något njutbart att vila i och beröras av.
								</p>
							</article>
						</div>
					</section>

					<!-- second section -->
					<section>
						<TabGroup justify="justify-center">
							<Tab bind:group={tabSet} name="tab1" value={0}>Älskade Solnedgång</Tab>
							<Tab bind:group={tabSet} name="tab2" value={1}>Smålands Trädgård</Tab>
							<Tab bind:group={tabSet} name="tab3" value={2}>Inredning</Tab>
							<Tab bind:group={tabSet} name="tab4" value={3}>Tänkvärt</Tab>
							<!-- Tab Panels --->
							<svelte:fragment slot="panel">
								{#if tabSet === 0}
									<div class="gap-2">
										<div class="flex p-2 lg:items-center lg:justify-between">
											<div class="flex-1">
												<!-- Älskade solnedgång -->
												<section>
													<div class="mx-auto max-w-screen-xl px-4 sm:px-6 sm:py-18 lg:px-8">
														<div class="grid sm:grid-flow-row md:grid-flow-row lg:grid-flow-col">
															<div class="lg:py-2 p-2">
																<div class="max-w-3xl py-4">
																	<h2 class="text-3xl font-bold sm:text-4xl">Älskade solnedgång</h2>
																</div>
																<article class="space-y-4">
																	<p>
																		Under åren har vi fått förmånen att njuta av den ena
																		solnedgången vackrare än den andra. Vi vill därför dela några av
																		bilderna med dig och hoppas att du snart får möjlighet att komma
																		till Hagablänket så att du själv får se och njuta av de fina
																		sommarkvällarna.
																	</p>
																</article>
															</div>
															<div class="lg:h-full">
																<!-- Carussel -->

																<div class="card p-4 grid grid-cols-[auto_1fr_auto] items-center">
																	<!-- Full Images -->
																	<div
																		bind:this={elemCarousel}
																		class="snap-x snap-mandatory scroll-smooth flex overflow-x-auto"
																	>
																		{#each solnedgångKarusellIds as solnedgångKarusellId}
																			<img
																				class="snap-center w-[1024px] rounded-container-token"
																				src={solnedgångKarusellId}
																				alt={solnedgångKarusellId}
																				loading="lazy"
																			/>
																		{/each}
																	</div>
																</div>

																<div class="card p-4 grid grid-cols-6 gap-4">
																	{#each solnedgångKarusellIds as solnedgångKarusellId, i}
																		<button type="button" on:click={() => carouselThumbnail(i)}>
																			<img
																				class="rounded-container-token"
																				src={solnedgångKarusellId}
																				alt={solnedgångKarusellId}
																				loading="lazy"
																			/>
																		</button>
																	{/each}
																</div>

																<!-- end of carussel -->
															</div>
														</div>
													</div>
												</section>
											</div>
										</div>
									</div>
								{:else if tabSet === 1}
									<!-- Smålands trädgård -->
									<div class="gap-2">
										<div class="flex p-2 lg:items-center lg:justify-between">
											<div class="flex-1">
												<section>
													<div class="mx-auto max-w-screen-xl px-4 sm:px-6 sm:py-18 lg:px-8">
														<div class="grid sm:grid-flow-row md:grid-flow-row lg:grid-flow-col">
															<div class="lg:py-2 p-2">
																<div class="max-w-3xl py-4">
																	<h2 class="text-3xl font-bold sm:text-4xl">Smålands trädgård</h2>
																</div>
																<article class="space-y-4">
																	<p>
																		Hagablänket är ett av många smultronställen i det natursköna
																		området Smålands Trädgård runt sjön Saljen. Vissa tider på året
																		är det som ett naturens skafferi med svamp och bär av olika
																		slag. Andra årstider bjuder på skir grönska, sprakande
																		höstfärger eller gnistrande rimfrost. Vi önskar att du snart ska
																		få se det vackra med egna ögon. Tills dess får du njuta av
																		bilderna.
																	</p>
																</article>
															</div>
															<div class="lg:h-full">
																<!-- Carussel -->

																<div class="card p-4 grid grid-cols-[auto_1fr_auto] items-center">
																	<!-- Full Images -->
																	<div
																		bind:this={elemCarousel}
																		class="snap-x snap-mandatory scroll-smooth flex overflow-x-auto"
																	>
																		{#each trädgårdKarusellIds as trädgårdKarusellId}
																			<img
																				class="snap-center w-[1024px] rounded-container-token"
																				src={trädgårdKarusellId}
																				alt={trädgårdKarusellId}
																				loading="lazy"
																			/>
																		{/each}
																	</div>
																</div>

																<div class="card p-4 grid grid-cols-6 gap-4">
																	{#each trädgårdKarusellIds as trädgårdKarusellId, i}
																		<button type="button" on:click={() => carouselThumbnail(i)}>
																			<img
																				class="rounded-container-token"
																				src={trädgårdKarusellId}
																				alt={trädgårdKarusellId}
																				loading="lazy"
																			/>
																		</button>
																	{/each}
																</div>

																<!-- end of carussel -->
															</div>
														</div>
													</div>
												</section>
											</div>
										</div>
									</div>
								{:else if tabSet === 2}
									<!-- Inredning -->
									<div class="gap-2">
										<div class="flex p-2 lg:items-center lg:justify-between">
											<div class="flex-1">
												<section>
													<div class="mx-auto max-w-screen-xl px-4 sm:px-6 sm:py-18 lg:px-8">
														<div class="grid sm:grid-flow-row md:grid-flow-row lg:grid-flow-col">
															<div class="lg:py-2 p-2">
																<div class="max-w-3xl py-4">
																	<h2 class="text-3xl font-bold sm:text-4xl">Inredning</h2>
																</div>
																<article class="space-y-4">
																	<p>
																		Inredningsdetaljer Skogslugnet Det är inte oviktigt hur ett hem
																		är inrett. Därför har vi gjort vårt yttersta för att Hagablänket
																		ska erbjuda något njutbart även de dagar det känns bäst att
																		stanna inomhus. En sprakande brasa eller en genomtänkt
																		dekoration, en vacker bukett eller något gammalt och nött. Någon
																		har sagt att kärleken ligger i de små detaljerna. Ibland är det
																		de minsta detaljerna som gör det största intrycket. Hämta
																		inspiration eller låt blicken bara vila.
																	</p>
																</article>
															</div>
															<div class="lg:h-full">
																<!-- Carussel -->

																<div class="card p-4 grid grid-cols-[auto_1fr_auto] items-center">
																	<!-- Full Images -->
																	<div
																		bind:this={elemCarousel}
																		class="snap-x snap-mandatory scroll-smooth flex overflow-x-auto"
																	>
																		{#each inredningKarusellIds as inredningKarusellId}
																			<img
																				class="snap-center w-[1024px] rounded-container-token"
																				src={inredningKarusellId}
																				alt={inredningKarusellId}
																				loading="lazy"
																			/>
																		{/each}
																	</div>
																</div>

																<div class="card p-4 grid grid-cols-6 gap-4">
																	{#each inredningKarusellIds as inredningKarusellId, i}
																		<button type="button" on:click={() => carouselThumbnail(i)}>
																			<img
																				class="rounded-container-token"
																				src={inredningKarusellId}
																				alt={inredningKarusellId}
																				loading="lazy"
																			/>
																		</button>
																	{/each}
																</div>

																<!-- end of carussel -->
															</div>
														</div>
													</div>
												</section>
											</div>
										</div>
									</div>
								{:else if tabSet === 3}
									<!-- Tänkvärt -->
									<div class="gap-2">
										<div class="flex p-2 lg:items-center lg:justify-between">
											<div class="flex-1">
												<section>
													<div class="mx-auto max-w-screen-xl px-4 sm:px-6 sm:py-18 lg:px-8">
														<div class="grid sm:grid-flow-row md:grid-flow-row lg:grid-flow-col">
															<div class="lg:py-2 p-2">
																<div class="max-w-3xl py-4">
																	<h2 class="text-3xl font-bold sm:text-4xl">Tänkvärt</h2>
																</div>
																<article class="space-y-4">
																	<p>
																		”Oron upphör där tron tar vid” ”Det är när vi kommer till slutet
																		av vår egen förmåga, accepterar våra svagheter och erkänner att
																		vi behöver Guds hjälp som vi upptäcker vår fulla potential.” ”Om
																		vi förstod hur högt Gud älskar alla vars liv berör våra, skulle
																		vi också anstränga oss mer för att älska dem.” ”Överträffa
																		varandra i ömsesidig aktning.” ”Inget hjärta är så hårt att inte
																		Guds kärlek kan beröra och förändra det.”
																	</p>
																</article>
															</div>
															<div class="lg:h-full">
																<!-- Carussel -->

																<div class="card p-4 grid grid-cols-[auto_1fr_auto] items-center">
																	<!-- Full Images -->
																	<div
																		bind:this={elemCarousel}
																		class="snap-x snap-mandatory scroll-smooth flex overflow-x-auto"
																	>
																		{#each tänkvärtKarusellIds as tänkvärtKarusellId}
																			<img
																				class="snap-center w-[1024px] rounded-container-token"
																				src={tänkvärtKarusellId}
																				alt={tänkvärtKarusellId}
																				loading="lazy"
																			/>
																		{/each}
																	</div>
																</div>

																<div class="card p-4 grid grid-cols-6 gap-4">
																	{#each tänkvärtKarusellIds as tänkvärtKarusellId, i}
																		<button type="button" on:click={() => carouselThumbnail(i)}>
																			<img
																				class="rounded-container-token"
																				src={tänkvärtKarusellId}
																				alt={tänkvärtKarusellId}
																				loading="lazy"
																			/>
																		</button>
																	{/each}
																</div>

																<!-- end of carussel -->
															</div>
														</div>
													</div>
												</section>
											</div>
										</div>
									</div>
								{/if}
							</svelte:fragment>
						</TabGroup>
					</section>
					<!-- end of second section -->

					<Footer />
				</div>
			</div>
		</div>
	</body>
</html>
