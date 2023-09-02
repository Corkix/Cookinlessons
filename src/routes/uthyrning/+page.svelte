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
					<Uthyrning />

					<section class="p-10 flex-row">
						<div class="card px-1 pb-8 space-y-4">
							<h2>Endagsbesök</h2>

							<img src="https://hagablanket.se/bilder/endag1.jpg" alt="" />

							<p>
								Under lågsäsong tar vi emot grupper av olika slag för kortare besök. Det kan vara
								arbetsgruppen, styrelsen eller pensionärsföreningen som vill ha en heldag i
								Hagablänket. Det kan vara tjejgänget, jaktlaget eller sångkören som vill komma en
								halvdag eller bara över kvällen. Det kan vara någon som vill ordna hajk för sina
								konfirmander, fira sin högtidsdag med släkten eller kanske ordna ett litet och
								mysigt bröllop med de närmaste. Catering och logi kan ordnas. Vi berättar gärna
								vilka möjligheter som finns.
							</p>
							<p>
								Hagablänket är en fridfull plats med natursköna omgivningar och den mycket speciella
								inredningen kan få idéerna att flöda. Vi vill vara en plats som inbjuder till både
								vila och kreativitet, en plats där du kan känna dig hemma. Hör av dig med din idé så
								försöker vi hitta ett upplägg och datum som passar för just ditt besök och din
								grupp.
							</p>
							<p>
								Vid varje besök erbjuds möjligheten att få en guidad rundvandring och höra den
								märkliga berättelsen om hur Hagablänket kom till. Det kan bli en spännande och
								innehållsrik programpunkt. Även andra enklare aktiviteter kan ingå vid behov. Varmt
								välkommen att landa hos oss i Hagablänket!
							</p>
						</div>
						<div class="card px-1 pb-8 space-y-4">
							<h2>Retreater och vila</h2>

							<img src="https://hagablanket.se/bilder/solnedgang-hangmatta.jpg" alt="" />

							<p>
								Under lågsäsong tar vi emot grupper av olika slag för kortare besök. Det kan vara
								arbetsgruppen, styrelsen eller pensionärsföreningen som vill ha en heldag i
								Hagablänket. Det kan vara tjejgänget, jaktlaget eller sångkören som vill komma en
								halvdag eller bara över kvällen. Det kan vara någon som vill ordna hajk för sina
								konfirmander, fira sin högtidsdag med släkten eller kanske ordna ett litet och
								mysigt bröllop med de närmaste. Catering och logi kan ordnas. Vi berättar gärna
								vilka möjligheter som finns.
							</p>
							<p>
								Hagablänket är en fridfull plats med natursköna omgivningar och den mycket speciella
								inredningen kan få idéerna att flöda. Vi vill vara en plats som inbjuder till både
								vila och kreativitet, en plats där du kan känna dig hemma. Hör av dig med din idé så
								försöker vi hitta ett upplägg och datum som passar för just ditt besök och din
								grupp.
							</p>
							<p>
								Vid varje besök erbjuds möjligheten att få en guidad rundvandring och höra den
								märkliga berättelsen om hur Hagablänket kom till. Det kan bli en spännande och
								innehållsrik programpunkt. Även andra enklare aktiviteter kan ingå vid behov. Varmt
								välkommen att landa hos oss i Hagablänket!
							</p>
						</div>
					</section>
					<Footer />
				</div>
			</div>
		</div>
	</body>
</html>
