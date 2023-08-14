<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import Uthyrning from '$lib/components/Uthyrning.svelte';

	let elemCarousel: HTMLDivElement;
	const unsplashIds = [
		'https://hagablanket.se/bilder/skogslugnet-och-sjomagasinet.jpg',
		'https://hagablanket.se/bilder/sjomagasinet.jpg',
		'https://hagablanket.se/wp-content/uploads/2021/06/Siluetter-i-solnedgang.jpg',
		'https://hagablanket.se/wp-content/uploads/2021/05/hagablanket-skogslugnet-2.jpg',
		'https://hagablanket.se/wp-content/uploads/2021/05/skogslugnet13.jpg',
		'https://hagablanket.se/wp-content/uploads/2021/06/rakmacka-1.jpg'
	];

	function carouselLeft(): void {
		const x =
			elemCarousel.scrollLeft === 0
				? elemCarousel.clientWidth * elemCarousel.childElementCount // loop
				: elemCarousel.scrollLeft - elemCarousel.clientWidth; // step left
		elemCarousel.scroll(x, 0);
	}

	function carouselRight(): void {
		const x =
			elemCarousel.scrollLeft === elemCarousel.scrollWidth - elemCarousel.clientWidth
				? 0 // loop
				: elemCarousel.scrollLeft + elemCarousel.clientWidth; // step right
		elemCarousel.scroll(x, 0);
	}

	function carouselThumbnail(index: number) {
		elemCarousel.scroll(elemCarousel.clientWidth * index, 0);
	}
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
			<!-- Hero -->
			<section class="bg-gray-50">
				<div class="">
					<img
						alt="lingon buske med en sjö och skog i bakgrunden"
						src="https://hagablanket.se/wp-content/uploads/2022/12/Sidhuvud-Hagablanket-Smal.jpg"
						class="w-full h-full"
					/>
				</div>
			</section>
			<!-- End of Hero -->
			<div class="flex p-2 lg:items-center lg:justify-between">
				<div class="flex-1">
					<!-- fist section  -->
					<section>
						<div class="mx-auto max-w-screen-xl px-4 py-14 sm:px-6 sm:py-18 lg:px-8">
							<div class="grid sm:grid-flow-row md:grid-flow-row lg:grid-flow-col">
								<div class="lg:h-full">
									<!-- Carussel -->

									<div class="card p-4 grid grid-cols-[auto_1fr_auto] items-center">
										<!-- Full Images -->
										<div
											bind:this={elemCarousel}
											class="snap-x snap-mandatory scroll-smooth flex overflow-x-auto"
										>
											{#each unsplashIds as unsplashId}
												<img
													class="snap-center w-[1024px] rounded-container-token"
													src={unsplashId}
													alt={unsplashId}
													loading="lazy"
												/>
											{/each}
										</div>
									</div>

									<div class="card p-4 grid grid-cols-6 gap-4">
										{#each unsplashIds as unsplashId, i}
											<button type="button" on:click={() => carouselThumbnail(i)}>
												<img
													class="rounded-container-token"
													src={unsplashId}
													alt={unsplashId}
													loading="lazy"
												/>
											</button>
										{/each}
									</div>

									<!-- end of carussel -->
								</div>
								<div class="lg:py-2 p-2">
									<div class="max-w-3xl py-4">
										<h2 class="text-3xl font-bold sm:text-4xl">Landa i vackra Hagablänket</h2>
									</div>
									<article class="space-y-4">
										<p>
											Mitt i natursköna Smålands Trädgård vid sjön Saljen, ligger Hagablänket – ett
											blänk av Småländsk natur när den är som bäst! Det är en plats med många
											möjligheter och uthyrning av två nybyggda hus med självhushåll. Sjömagasinet
											som erbjuder 13 bäddar och Skogslugnet med plats för upp till 17 gäster. Husen
											kan hyras separat eller tillsammans och sängarna står alltid bäddade med vita
											lakan när ni kommer.
										</p>

										<p>
											Omgivningarna bjuder på vila och rekreation i skog och mark. Här finns fiske,
											bad, härliga båtturer, stillhet och tystnad. Hagablänket passar för
											barnfamiljer, medarbetardagar, mindre läger, semester eller högtider med hela
											släkten – eller varför inte bara en mysig helg på tu man hand?
										</p>

										<p>
											Här på hemsidan hoppas vi att du ska hitta bilder och information som gör dig
											glad och nyfiken. Läs mer under flikarna, titta på bilderna och hör av dig med
											frågor eller bokningsförfrågan. Vill du komma och titta på plats och höra den
											märkliga berättelsen om Hagablänket så är du varmt välkommen.
										</p>

										<p>Vi bjuder på en kopp kaffe!</p>

										<p>Lenette & Sigge Ahnstedt</p>
									</article>
								</div>
							</div>
						</div>
					</section>
					<!-- end of first section -->

					<Uthyrning />

					<section class="p-4 flex-row">
						<div class="card p-4 px-10">
							Vill ni bara boka en dag eller kväll finns mer information under Endagsbesök. Har du
							behov av vila och återhämtning kan du välja att läsa under Retreater/vila. I
							Hagablänket finns också Kapellet. Det är en timmer-stuga med ett stort rum och ett
							mindre samtalsrum som, så fort det blivit klart, kommer att kunna användas. Vårt
							smultronställe är en plats med många möjligheter för gäster med olika behov. Under de
							olika flikarna kan du se bilder och läsa mer om respektive boende.
						</div>
					</section>
					<Footer />
				</div>
			</div>
		</div>
	</body>
</html>
