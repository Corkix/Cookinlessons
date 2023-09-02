<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import Uthyrning from '$lib/components/Uthyrning.svelte';

	let elemCarousel: HTMLDivElement;
	const karusellIds = [
		'https://hagablanket.se/wp-content/uploads/2021/05/skogslugnet1.jpg',
		'https://hagablanket.se/bilder/skogslugnet2',
		'https://hagablanket.se/bilder/skogslugnet3',
		'https://hagablanket.se/bilder/skogslugnet4',
		'https://hagablanket.se/bilder/skogslugnet5',
		'https://hagablanket.se/bilder/skogslugnet6'
	];

	const bildGalleriIds = [
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
						src="https://hagablanket.se/wp-content/uploads/2021/05/skogslugnet1.jpg"
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
										<h2 class="text-3xl font-bold sm:text-4xl">Skogslugnet</h2>
									</div>
									<article class="space-y-4">
										<p>
											Skogslugnet är det första huset som byggdes i Hagablänket. Det ligger med fin
											utsikt över sjön och 14+3 bäddplatser. På bottenvåningen finns Logen på 150m2
											med fullutrustat kök och stort allrum med sjöutsikt, matbord, soffor,
											braskamin samt utgång till altanen och totalt 7 bäddar. Två av dem hittar du i
											den vackra Sängkammaren med plats för två och lika vacker utsikt. Sovskrubben
											är det mysiga lilla enkelrummet under trappan och i Dubbelskrubben finns
											husets enda våningssäng. I allrummet finns två extrabäddar, Himmelsängen och
											Fönsternischen, med mysiga draperier att gömma sig bakom. Det rymliga
											badrummet har både toalett, handfat, badkar, dusch, fantastisk sjöutsikt och
											kristallkrona i taket. Dessutom har gäster också tillgång till en allmän
											Servicedel i direkt anslutning till Logen. Där finns tvättmaskin, groventré,
											ett extra kök, micro och tillgång till en extra toalett och dusch samt
											skötbord, vid behov.
										</p>

										<p>
											På övervåningen finns Rännet och Loftet med 10 bäddar, ytterligare 150m2 och
											ännu vackrare utsikt. Rännet har egen ingång från en gallertrappa och stort
											allrum med kamin, soffor, eget kök och matplats. Från allrummet kan man njuta
											av sjön och solnedgången mellan trädstammarna. Hösthimlen är Rännets mysiga
											dubbelrum och även Vårvinden med två bäddar går att möblera som dubbelrum vid
											behov. I Vintervilan finns lite annorlunda detaljer och en enkelsäng och i
											allrummet hittar du Sommarsolen, en av extrabäddarna. Toalett med dusch finns
											också.
										</p>

										<p>
											På Loftet precis intill, finns ännu ett litet allrum med soffa, fåtöljer och
											två bäddar som kan användas separat eller som dubbelsäng. Snickerboa och
											Sjöboa är de två små mysiga enkelrummen i direkt anslutning till Loftet.
											Trisseboa är det lilla dasset med toalett och handfat. Från loftet går en
											separat trappa ner till Servicedelen där kök, dusch och skötbord finns inom
											räckhåll. Bra för familjer med lite mindre barn. En eller två barnsängar kan
											också få plats på Loftet vid behov.
										</p>

										<p>
											Ni bor mitt i skogen med bara 100 meter till sjön med grillplats, hyrbåt och
											härlig skogsstrand. Grillmöjligheter och flera uteplatser finns även i
											anslutning till huset. Kom och upplev lugnet och friden i de Småländska
											skogarna. Sängarna står alltid bäddade med vita lakan när ni kommer. Skogen,
											badplatsen och grillplatsen är till för alla och får användas av fler än
											gästerna. Efter överenskommelse kan vi ordna så att kyl och skafferi är fyllt
											efter era önskemål. Beställda varor betalas senast vid ankomst. Våra
											uthyrningsvillkor finns under en egen flik och ska läsas innan bokning.
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
