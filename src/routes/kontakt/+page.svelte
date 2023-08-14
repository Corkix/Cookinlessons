<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import { TabGroup, Tab } from '@skeletonlabs/skeleton';

	let tabSet: number = 0;

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
		'https://hagablanket.se/bilder/skogslugnet9'
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
						alt=""
						src="https://hagablanket.se/wp-content/uploads/2022/12/Sidhuvud-Hagablankets-Undersidor.jpg"
						class="w-full h-full"
					/>
				</div>
			</section>
			<!-- End of Hero -->
			<div class="flex p-2 lg:items-center lg:justify-between">
				<div class="flex-1">
					<!-- fist section  -->
					<section>
						<div class="flex mx-auto max-w-screen-xl px-4 py-8 sm:px-6 sm:py-18 lg:px-8">
							<div class="grid sm:grid-flow-row md:grid-flow-row lg:grid-flow-col">
								<div class="lg:py-2 p-2">
									<div class="max-w-3xl py-4">
										<h2 class="text-3xl font-bold sm:text-4xl">Om oss</h2>
									</div>
									<article class="space-y-4">
										<p>
											Vi som hyr ut Hagablänket heter Lenette & Sigge Ahnstedt. En dröm har blivit
											verklighet men vägen dit har varit lång. Nu står husen klara mitt i en
											underbar omgivning, bara 100 meter från sjön Saljen i Stenberga och vi vill
											gärna att fler får glädje av vårt alldeles egna smultronställe!
										</p>

										<p>
											Vilka är då vi? Lenette såg dagens ljus 1975 och gården Haga, där Hagablänket
											byggts upp, är hennes föräldragård. Hon är florist och musiker med många
											strängar på sin lyra. Genom företaget SOLFJÄT-Blommor & Sång erbjuder hon
											blommor, sång och musik till både bröllop och begravning. Hon har spelat in en
											CD-skiva med dottern Sara, född 1999, som nu är mamma till två fina grabbar
											och bor med man och barn lite norr om Göteborg i Alafors. Lenette har gett ut
											ett par böcker åt en släkting och tillsammans med sin bror gjort en film om
											sin föräldragård, Hemma på Haga marker. De senaste åren har hon varit
											byggledare i Hagablänket.
										</p>
									</article>
								</div>

								<div class="lg:h-full">
									<!-- Carussel -->

									<div class="card p-4 grid grid-cols-[auto_1fr_auto] items-center">
										<!-- Full Images -->
										<div class="snap-x snap-mandatory scroll-smooth flex overflow-x-auto">
											<img
												class="snap-center w-[1024px] rounded-container-token"
												src="https://www.dagen.se/resizer/ytfy7aVX5lJyBFq9o35a2Ya7g8w=/800x0/filters:format(jpg):quality(70):focal(705x493:715x503)/cloudfront-eu-central-1.images.arcpublishing.com/mentormedier/I4EARG7ZJN32LAPFM2MKR2OA7U.jpg"
												alt=""
												loading="lazy"
											/>
										</div>
									</div>
									<!-- end of carussel -->
								</div>
							</div>
						</div>
					</section>
					<!-- end of first section -->

					<section>
						<div class="card p-4 px-10">
							<div class="max-w-screen-xl px-4 py-8 mx-auto sm:py-12 sm:px-6 lg:px-8">
								<div class="grid grid-cols-1 gap-4 lg:grid-cols-2 lg:items-stretch">
									<div class="grid p-6 rounded place-content-center sm:p-8">
										<div class="max-w-md mx-auto text-center lg:text-left">
											<header>
												<h2 class="text-xl font-bold sm:text-3xl">Stöd oss</h2>
											</header>

											<form class="w-full max-w-lg">
												<div class="flex flex-wrap -mx-3 mb-6">
													<div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
														<label
															class="block uppercase tracking-wide text-xs font-bold mb-2"
															for="grid-first-name"
														>
															Förnamn
														</label>
														<input
															class="appearance-none block w-full bg-gray-200 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
															id="grid-first-name"
															type="text"
															placeholder="Jane"
														/>
													</div>
													<div class="w-full md:w-1/2 px-3">
														<label
															class="block uppercase tracking-wide text-xs font-bold mb-2"
															for="grid-last-name"
														>
															Efternamn
														</label>
														<input
															class="appearance-none block w-full bg-gray-200 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
															id="grid-last-name"
															type="text"
															placeholder="Jane"
														/>
													</div>
												</div>
												<div class="flex flex-wrap -mx-3 mb-6">
													<div class="w-full px-3">
														<label
															class="block uppercase tracking-wide text-xs font-bold mb-2"
															for="grid-password"
														>
															E-post
														</label>
														<input
															class="appearance-none block w-full bg-gray-200 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
															id="grid-password"
															type="password"
															placeholder="Jane"
														/>
													</div>
												</div>
											</form>

											<h4>Stort tack för ditt stöd!</h4>
										</div>
									</div>
									<div class="grid p-6 rounded place-content-center sm:p-8">
										<div class="max-w-md mx-auto text-center lg:text-left">
											<img
												src="https://hagablanket.se/wp-content/uploads/2021/06/DSF3056.jpg"
												alt=""
											/>
										</div>
									</div>
								</div>
							</div>
						</div>
					</section>

					<Footer />
				</div>
			</div>
		</div>
	</body>
</html>
