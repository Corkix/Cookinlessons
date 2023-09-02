<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import Uthyrning from '$lib/components/Uthyrning.svelte';

	let elemCarousel: HTMLDivElement;
	const karusellIds = [
		'https://hagablanket.se/bilder/vindskyddet1.jpeg',
		'https://hagablanket.se/bilder/vindskyddet2.jpeg',
		'https://hagablanket.se/bilder/gronskavidvattnet.jpg',
		'https://hagablanket.se/bilder/vidvattnet.jpg',
		'https://hagablanket.se/bilder/vindskyddetsolnedgang.jpg',
		'https://hagablanket.se/bilder/rosasolnedgang.jpeg'
	];

	const bildGalleriIds = [
		'https://hagablanket.se/bilder/vindskyddet1.jpeg',
		'https://hagablanket.se/bilder/vindskyddet2.jpeg',
		'https://hagablanket.se/bilder/gronskavidvattnet.jpg',
		'https://hagablanket.se/bilder/vidvattnet.jpg',
		'https://hagablanket.se/bilder/vindskyddetsolnedgang.jpg',
		'https://hagablanket.se/bilder/rosasolnedgang.jpeg'
	];

	function carouselThumbnail(index: number) {
		elemCarousel.scroll(elemCarousel.clientWidth * index, 0);
	}
</script>

<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Hagablänket</title>
	</head>
	<body class="flex flex-col">
		<div class="gap-2">
			<!-- Hero -->
			<section class="bg-gray-50">
				<div class="">
					<img alt="" src="https://hagablanket.se/bilder/vindskyddet1.jpeg" class="w-full h-full" />
				</div>
			</section>
			<!-- End of Hero -->
			<div class="flex p-2 lg:items-center lg:justify-between">
				<div class="flex-1">
					<!-- fist section  -->
					<section>
						<div class="mx-auto max-w-screen-xl px-4 py-8 sm:px-6 sm:py-18 lg:px-8">
							<div class="grid sm:grid-flow-row md:grid-flow-row lg:grid-flow-col">
								<div class="lg:py-2 p-2">
									<div class="max-w-3xl py-4">
										<h2 class="text-3xl font-bold sm:text-4xl">Vindskyddet</h2>
									</div>
									<article class="space-y-4">
										<p>
											Vårt mysiga vindskydd har gott om plats för 3-4 vuxna eller en barnfamilj. Det
											ligger med fantastisk utsikt över sjön och solnedgången. Där finns både
											taklampa och eluttag för laddning av mobilen och för 150kr/person och natt får
											du tillgång till vår Servicedel med toalett, dusch, enklare kök och
											tvättmaskin. Medtag egen sovsäck och liggunderlag/luftmadrass.
										</p>

										<p>
											Bokas direkt med oss i mån av plats, senast samma dag på telefon eller sms
											till 070-603 95 82. Skogen, badplatsen och grillplatsen är till för alla och
											får användas av fler än gästerna.
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
											{#each karusellIds as karusellId}
												<img
													class="snap-center w-[1024px] rounded-container-token"
													src={karusellId}
													alt={karusellId}
													loading="lazy"
												/>
											{/each}
										</div>
									</div>

									<div class="card p-4 grid grid-cols-6 gap-4">
										{#each karusellIds as karusellId, i}
											<button type="button" on:click={() => carouselThumbnail(i)}>
												<img
													class="rounded-container-token"
													src={karusellId}
													alt={karusellId}
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
					<!-- end of first section -->

					<section class="p-4 flex-row">
						<div class="lg:py-2 lg:mx-2 lg:px-20 p-2">
							<div class="max-w-3xl py-4">
								<h2 class="text-3xl font-bold sm:text-4xl">Pris</h2>
							</div>
							<article class="space-y-4">
								<p>
									Sjömagasinet hyrs ut minst 2-3 nätter i följd och i första hand hela veckor. Då
									prisläget påverkas av längden på vistelsen, tiden på året, eventuella storhelger
									samt antalet gäster det gäller så har vi valt att inte gå ut med några priser här
									på hemsidan. Vi ber er därför skicka ett mail med er förfrågan. Berätta gärna lite
									om er själva, syftet med er vistelse och hur många barn respektive vuxna ni är som
									vill komma så återkommer vi med ett prisförslag.
								</p>
							</article>

							<button
								type="button"
								class="btn variant-filled-primary px-12 py-3 mt-8 text-md font-medium"
								>Skicka en förfrågan</button
							>
						</div>
					</section>

					<section class="grid grid-cols-2 md:grid-cols-3 gap-4 p-4">
						{#each bildGalleriIds as bildGalleriId}
							<div>
								<img
									class="snap-center w-[1024px] rounded-container-token"
									src={bildGalleriId}
									alt={bildGalleriId}
									loading="lazy"
								/>
							</div>
						{/each}
					</section>

					<Uthyrning />

					<Footer />
				</div>
			</div>
		</div>
	</body>
</html>
