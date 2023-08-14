<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import Uthyrning from '$lib/components/Uthyrning.svelte';

	let elemCarousel: HTMLDivElement;
	const karusellIds = [
		'https://hagablanket.se/bilder/sjomagasinet.jpg',
		'https://hagablanket.se/bilder/sjomagasinet22.jpg',
		'https://hagablanket.se/bilder/sjomagasinet21.jpg',
		'https://hagablanket.se/bilder/sjomagasinet32.jpg',
		'https://hagablanket.se/bilder/sjomagasinet25.jpg',
		'https://hagablanket.se/bilder/sjomagasinet24.jpg'
	];

	const bildGalleriIds = [
		'https://hagablanket.se/bilder/sjomagasinet47.jpg',
		'https://hagablanket.se/bilder/sjomagasinet30.jpg',
		'https://hagablanket.se/bilder/sjomagasinet27.jpg',
		'https://hagablanket.se/bilder/sjomagasinet26.jpg',
		'https://hagablanket.se/bilder/sjomagasinet31.jpg',
		'https://hagablanket.se/bilder/sjomagasinet28.jpg',
		'https://hagablanket.se/bilder/sjomagasinet29.jpg',
		'https://hagablanket.se/bilder/sjomagasinet33.jpg',
		'https://hagablanket.se/bilder/sjomagasinet45.jpg',
		'https://hagablanket.se/bilder/sjomagasinet43.jpg',
		'https://hagablanket.se/bilder/sjomagasinet44.jpg',
		'https://hagablanket.se/bilder/sjomagasinet38.jpg'
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
						alt="Bild på Skogslunget med sin vita dörr"
						src="https://hagablanket.se/bilder/sjomagasinet.jpg"
						class="w-full h-full"
					/>
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
										<h2 class="text-3xl font-bold sm:text-4xl">Sjömagasinet</h2>
									</div>
									<article class="space-y-4">
										<p>
											Sjömagasinet är ett precis nybyggt hus med sjöutsikt och näst intill
											strandtomt. Där finns 10+3 bäddar och bara 100 meter från huset finns
											möjlighet till båt, bad och fiske. Ibland färgar solnedgången himlen och
											vattnet i skiftande färger.
										</p>

										<p>
											På bottenvåningen finns fullutrustat kök/allrum med sjöutsikt, matbord och
											soffor samt utgång mot sjön. Det vackra sovrummet har också en altandörr och
											vacker sjöutsikt samt plats för en barnsäng vid behov. Stort badrum med dusch
											precis intill och altandörr även därifrån.
										</p>

										<p>
											På vindsvåningen finns tre familjerum med snedtak och lite olika inredning.
											Östra sjösviten har dubbelsäng och en fullstor våningssäng samt en mindre
											barnsäng. Västra Sjösviten har en dubbelsäng samt en äldre, lite kortare 100
											år gammal säng med höga gavlar. Plats finns för en mindre barnsäng vid behov.
											Båda rummen har fransk balkong med utsikt över sjön. Stjärnhimlen är det
											tredje familjerummet som istället har takfönster och utsikt från dubbelsängen
											rakt upp mot stjärnhimlen. (Därför saknas möjlighet till mörkläggning) Rummet
											har tre fullstora bäddar och en extrabädd gömd bakom vackra allmogedörrar. En
											liten koja helt enkelt, med egen stjärnhimmel. Förutom sovrummen finns allrum
											och ett badrum med dusch och skötbord.
										</p>

										<p>
											På bottenvåningen av Sjömagasinet är skötsamma hundar välkomna. Inga djur får
											vistas på vindsvåningen eller i sängarna. Grill och flera uteplatser finns i
											direkt anslutning till huset och även vid sjön. Skogen, badplatsen och
											grillplatsen är till för alla och får användas av fler än gästerna.
											Sjömagasinet inrymmer även ett större garage/båthus och förrådsutrymmen. Efter
											överenskommelse kan vi ordna så att kyl och skafferi är fyllt efter era
											önskemål. Beställda varor betalas senast vid ankomst. Våra uthyrningsvillkor
											finns under en egen flik och ska läsas innan bokning.
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
