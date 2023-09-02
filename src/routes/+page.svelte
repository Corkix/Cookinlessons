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

					<section>
						<div class="lg:py-2 px-5 md:px-8 lg:px-72 p-2">
							<div class="max-w-3xl py-4">
								<h2 class="text-3xl font-bold sm:text-4xl">Omdömen</h2>
							</div>
							<article class="space-y-4">
								<p>
									”Ett unikt sommarboende, med en fantastisk hyresvärd. Lugnt, rofyllt, härlig
									solnedgång både från stranden och huset. Trevlig liten badstrand, lämplig för
									såväl barn som vuxna. Måste upplevas!”
								</p>

								<p>
									“Hagablänket I a wonderful place that we already miss about a week after. The
									combination of the grand, beautiful and well equipped houses with plenty of space,
									and the quite simply glorious nature surrounding both houses makes this a great
									catch to book. The beauty of Småland, the privacy of the area, whether you book
									both houses or only one, you´ll have apace and privacy both indoors and outdoors.
									The owners are very helpful with any questions you might have, nothing seems to be
									a problem. Last but very much not least: The bed are great!”
								</p>

								<p>
									”En mycket varm och genuin plats och atmosfär. Otroligt vackert beläget i skogen,
									vid sjön nedanför. Inredningen är mycket smakfull och har en personlig utformning
									som gör att man känner sig hemma och välkommen. Rekommenderar Hagablänket för
									flera aktiviteter som för din familj eller bara för att vara i denna fantastiska
									miljö av lugn och stressfri avskildhet.”
								</p>
								<p>
									“We had a simply wonderful week in Sjömagasinet. The surrounding glorious nature,
									the space in and outside of the house and the comfortably designed interiors were
									all so well suited for our group of couples and friends. The layout is well
									thought out with a big living-room and kitchen, made for big dinners and long
									conversations. The outside area is comfortable and beautiful with plenty of room
									and seating for big parties or smaller meals. A short walk takes you to the lake
									where we spent many hours just taking in the view. There is both a beach shore
									suitable for walking into the water as well as a pier with a sturdy ladder. We had
									rented the other house aswell but there was enough distance to enjoy privacy if
									only Sjömagasinet had been rented.”
								</p>

								<p>
									“Hagablänket is an ideal home for a family vacation, a family reunion, or even a
									club or business retreat. The spacious home is beautifully decorated and is as
									luxurious and pristine as one could ask. The wonderful and gracious owners of this
									vacation home, have spared no expense in making their guests feel comfortable and
									pampered. With the adjacent lake on the property there is also the opportunity for
									fishing, swimming, boating and lakeside barbeques. We highly recommend this
									property and assure you that you will love it and never want to leave!”
								</p>
							</article>
						</div>
					</section>

					<section class="p-4 flex-row">
						<div class="card p-4 px-10" />
					</section>
					<Footer />
				</div>
			</div>
		</div>
	</body>
</html>
