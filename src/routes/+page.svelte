<script lang="ts">
	import HomeImg from '$lib/images/Home.jpg';
	import loga from '$lib/images/hagalogo1.png';
	import SjoHus from '$lib/images/sjomagasinet.jpg';
	import SkogHus from '$lib/images/skogslugnet.jpg';
	import hero1 from '$lib/images/hero1.jpg';
	import hero2 from '$lib/images/hero2.jpg';
	import hero3 from '$lib/images/hero3.jpg';
	import hero4 from '$lib/images/hero4.jpg';
	import hero5 from '$lib/images/hero5.jpg';
	import hero6 from '$lib/images/hero6.jpg';

	let elemCarousel: HTMLDivElement;
	const unsplashIds = [hero1, hero2, hero3, hero4, hero5, hero6];

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
						src={HomeImg}
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

					<!-- second section -->
					<section>
						<div class="card p-4 px-10">
							<div class="max-w-screen-xl px-4 py-8 mx-auto sm:py-12 sm:px-6 lg:px-8">
								<div class="grid grid-cols-1 gap-4 lg:grid-cols-3 lg:items-stretch">
									<div class="grid p-6 rounded place-content-center sm:p-8">
										<div class="max-w-md mx-auto text-center lg:text-left">
											<header>
												<h2 class="text-xl font-bold sm:text-3xl">Uthyrning</h2>

												<p class="mt-4">
													Hos oss kan du sova lyxigt i sköna sängar mellan vita lakan eller enkelt i
													vårt mysiga vindskydd vid sjökanten. Våra två hus, Skogslugnet och
													Sjömagasinet, kan hyras separat eller tillsammans med en total kapacitet
													för upp till 25-30 gäster.
												</p>
											</header>
											<button
												type="button"
												class="btn variant-filled-primary px-12 py-3 mt-8 text-md font-medium"
											>
												Läs mer
											</button>
										</div>
									</div>

									<div class="lg:col-span-2 lg:py-8">
										<ul class="grid grid-cols-2 gap-4">
											<li>
												<a href="/sjohus" class="block group">
													<img
														src={hero2}
														alt=""
														class="object-cover w-full rounded aspect-square"
													/>

													<div class="mt-3">
														<h3 class="font-medium text-gray-900">Sjömagasinet</h3>
													</div>
												</a>
											</li>

											<li>
												<a href="/skoghus" class="block group">
													<img
														src={SkogHus}
														alt=""
														class="object-cover w-full rounded aspect-square"
													/>

													<div class="mt-3">
														<h3 class="font-medium text-gray-900">Skogslugnet</h3>
													</div>
												</a>
											</li>
										</ul>
									</div>
								</div>
							</div>
						</div>
					</section>
					<!-- end of second section -->

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
					<!-- Footer -->

					<footer class="bg-gray-100">
						<div class="mx-auto max-w-5xl px-4 py-10 sm:px-6 lg:px-8">
							<div class="flex justify-center">
								<img alt="Hagablänkets loga" src={loga} />
							</div>

							<article class="mx-auto mt-6 max-w-md text-center leading-relaxed">
								<h3>Hagablänket</h3>
								<p>070-603 95 82</p>

								<p>kontakt@hagablanket.se</p>

								<p>Stenberga Sänsleviken 1</p>
								<p>574 97, Vetlanda</p>
							</article>

							<ul class="mt-12 flex flex-wrap justify-center gap-6 md:gap-8 lg:gap-12">
								<li>
									<a class="text-gray-700 transition hover:text-gray-700/75" href="/"> Hem </a>
								</li>

								<li>
									<a class="text-gray-700 transition hover:text-gray-700/75" href="/">
										Uthyrning
									</a>
								</li>

								<li>
									<a class="text-gray-700 transition hover:text-gray-700/75" href="/"> Om oss </a>
								</li>

								<li>
									<a class="text-gray-700 transition hover:text-gray-700/75" href="/">
										Stenberga Missionsförsamling
									</a>
								</li>
							</ul>

							<ul class="mt-12 flex justify-center gap-6 md:gap-8">
								<li>
									<a
										href="/"
										rel="noreferrer"
										target="_blank"
										class="text-gray-700 transition hover:text-gray-700/75"
									>
										<span class="sr-only">Facebook</span>
										<svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
											<path
												fill-rule="evenodd"
												d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z"
												clip-rule="evenodd"
											/>
										</svg>
									</a>
								</li>
							</ul>
						</div>
						<div class="flex justify-center p-1">
							<p class="text-sm">Copyright © 2023 Hagablänket Alla rättigheter förbehållna</p>
						</div>
					</footer>
					<!-- End of Footer -->
				</div>
			</div>
		</div>
	</body>
</html>
