<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import { TabGroup, Tab } from '@skeletonlabs/skeleton';
	import swish from '$lib/images/File.jpg';

	let tabSet: number = 0;

	const bildGalleriVisionIds = [
		'https://hagablanket.se/bilder/skogslugnet7',
		'https://hagablanket.se/bilder/skogslugnet8',
		'https://hagablanket.se/bilder/skogslugnet9'
	];
	const bildGalleriKortaIds = [
		'https://hagablanket.se/bilder/stentrappa.jpeg',
		'https://hagablanket.se/bilder/IMG_20180709_213610.jpeg',
		'https://hagablanket.se/bilder/skogslugnet4.jpg'
	];
	const bildGalleriLangaIds = [
		'https://hagablanket.se/bilder/Dagenartikel-Hagablanket_Sida_1.jpg',
		'https://hagablanket.se/bilder/stenarvidsjon.jpeg',
		'https://hagablanket.se/bilder/Dagenartikel-Hagablanket_Sida_2.jpg'
	];
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
										<h1 class="text-3xl font-bold sm:text-4xl">Om oss</h1>
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

						<section class="p-4 flex-col">
							<div class="lg:py-2 lg:mx-2 lg:px-20 p-2">
								<article class="space-y-4">
									<p>
										Sigge föddes 1966 på en gård i Skepperstad, strax utanför Sävsjö fem mil
										härifrån, som den yngste av tio syskon. Han jobbar som drifttekniker på Njudung
										Energi i Vetlanda och på fritiden kopplar han gärna av med lite fiske, helst
										trolling. I den mån han hinner hjälper han till med olika göromål i Hagablänket.
										Han har barnasinnet kvar, är en omtyckt scoutledare och stolt morfar till två
										barnbarn. Någon har sagt: Det konstigaste är inte att själv bli morfar, det
										konstigaste är att vakna upp bredvid mormor…
									</p>

									<p>
										Tillsammans med Lenette leder han nu Äktenskapsretreaterna i Hagablänket. Båda
										är sedan många år engagerade i den lilla missionsförsamlingen i Stenberga som
										ofta förlägger sin verksamhet till Hagablänket.
									</p>

									<p>
										Vi bor bara några kilometer bort i den lilla byn Smålands Farstorp längs väg 125
										och kan därför finnas tillgängliga så mycket som önskas. Där bor vi tillsammans
										med våra två yngsta barn, David som är född 2001 och Josef som är född 2006. Har
										vi tid och möjlighet bjuder vi gärna på en båttur, fisketur eller varför inte
										lite åkning med ringar efter båten för den som vågar. Något av det bästa vi vet
										är att få dela med oss av den märkliga berättelsen om hur Hagablänket kom till.
										Fråga oss så berättar vi gärna!
									</p>
								</article>
							</div>
						</section>
					</section>
					<!-- end of first section -->

					<section class="p-4 flex-col">
						<div class="lg:py-2 lg:mx-2 lg:px-20 p-2">
							<TabGroup justify="justify-center">
								<Tab bind:group={tabSet} name="tab1" value={0}>Visionen</Tab>
								<Tab bind:group={tabSet} name="tab2" value={1}>Den korta berättelsen</Tab>
								<Tab bind:group={tabSet} name="tab3" value={2}>Den långa berättelsen</Tab>

								<!-- Tab Panels --->
								<svelte:fragment slot="panel">
									{#if tabSet === 0}
										<section class="grid grid-cols-2 md:grid-cols-3 gap-4 p-4">
											{#each bildGalleriVisionIds as bildGalleriId}
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
										<div class="gap-2">
											<div class="flex p-2 lg:items-center lg:justify-between">
												<div class="flex-1">
													<section>
														<div class="max-w-3xl py-4">
															<h2 class="text-3xl font-bold sm:text-4xl">Visionen</h2>
														</div>
														<article class="space-y-4">
															<p>
																I Stenberga, mitt i natursköna Smålands Trädgård vid sjön Saljen,
																byggs just nu en rekreationsplats på Guds uppdrag. Vi är så
																tacksamma för förtroendet att få vara en del av detta. Ändå vet vi
																inte riktigt vad Gud har tänkt eftersom vi bara får veta ett steg i
																taget då både visionen och platsen tillhör Honom.
															</p>
															<p>
																När Skogslugnet, ett uthyrningshus med 17 bäddar, skulle byggas 2016
																fick vi ett bibelord: ”Detta är Herrens eget verk – det står för
																våra ögon som ett under” och det gör det verkligen! När
																Sjömagasinet, ett hus med 13 bäddar, garage och båthus, byggdes med
																hast 2020, gav han oss ordet: ”Herren skapade och det blev – han
																befallde och det stod där” och efter knappt fyra månader stod det
																klart för att ta emot de första gästerna! Inom en snar framtid tror
																vi också att ett Kapell och samtalsrum står redo att användas. I
																allt detta är vi helt beroende av förböner och att Herren förser med
																de resurser som behövs, precis som han lovat.
															</p>
															<p>
																Vår bön är att Hagablänket ska få vara en plats där människor får
																känna Guds frid och ges möjlighet att komma närmare Jesus Kristus
																som själv säger: ”Jag är vägen, sanningen och livet – ingen kommer
																till Fadern (Gud) utom genom mig.”
															</p>
															<p>
																Hör av dig om du vill veta mer eller komma på ett besök! Vill du
																hjälpa oss att sprida vår vision till fler så mailar eller skickar
																vi gärna vårt Visionsblad till dig. Bara kontakta oss!
															</p>
														</article>

														<article class="pt-4 space-y-1">
															<p>Guds välsignelse önskar vi dig!</p>
															<p>Lenette & Sigge Ahnstedt</p>
														</article>
													</section>
												</div>
											</div>
										</div>
									{:else if tabSet === 1}
										<section class="grid grid-cols-2 md:grid-cols-3 gap-4 p-4">
											{#each bildGalleriKortaIds as bildGalleriId}
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
										<div class="gap-2">
											<div class="flex p-2 lg:items-center lg:justify-between">
												<div class="flex-1">
													<section>
														<div class="max-w-3xl py-4">
															<h2 class="text-3xl font-bold sm:text-4xl">Den korta berättelsen</h2>
														</div>
														<article class="space-y-4">
															<p>
																Det är nästan omöjligt att sammanfatta historien om Hagablänket i en
																kort berättelse. Det har hänt så otroligt mycket märkliga grejer och
																mirakler de senaste åren att vi omöjligt kan få med allt på några
																rader. Utan Guds hjälp och tydliga instruktioner hade inte något av
																husen i Hagablänket kommit till och eftersom många människor redan
																fått glädje av platsen så är vi glada att vi mot allt sunt förnuft
																bildligt talat, vågade ta klivet över relingen och börja gå på
																vatten.
															</p>

															<p>
																Fram till början av 2016 var det bara skog och vildmark där
																Hagablänket nu ligger. Det enda som fanns var vindskyddet vid sjön,
																badplatsen och en liten skogsväg som ledde dit. Bara ett år senare
																hade skogen tagits ner, vatten sprungit fram ur berget, elektricitet
																grävts ner en sträcka på närmare en kilometer i stenig mark, vägar
																byggts, tillstånd sökts och det första huset, Skogslugnet,
																mirakulöst kommit på plats.
															</p>
															<p>
																2018 var byggnaden helt klar och luften gick nästan ur oss efter en
																mycket intensiv byggperiod. Vad vi inte visste då var att vi två år
																senare skulle ha byggt ytterligare ett stort hus och vara på god väg
																med den tredje byggnaden i Hagablänket, denna gång helt utan några
																egna ekonomiska medel. Så trots en mänskligt sett helt omöjlig
																situation fortsätter Gud att uppmana oss att färdigställa platsen.
																Varje steg vi tar är ett steg i tro och mänsklig galenskap. Ganska
																ofta frågar vi oss hur vi hamnade här men hittills har Gud visat oss
																ett steg i taget, även om vi fortfarande inte riktigt vet syftet med
																denna mycket märkliga resa.
															</p>
															<p>
																Kommer du på besök berättar vi gärna mer och en vacker dag skriver
																vi nog en bok. Tills dess kan du följa oss på vår facebooksida
																Hagablänket.
															</p>
														</article>
													</section>
												</div>
											</div>
										</div>
									{:else if tabSet === 2}
										<section class="grid grid-cols-2 md:grid-cols-3 gap-4 p-4">
											{#each bildGalleriLangaIds as bildGalleriId}
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
										<div class="gap-2">
											<div class="flex p-2 lg:items-center lg:justify-between">
												<div class="flex-1">
													<section>
														<div class="max-w-3xl py-4">
															<h2 class="text-3xl font-bold sm:text-4xl">Den långa berättelsen</h2>
														</div>
														<article class="space-y-4">
															<p>
																Den långa berättelsen om Hagablänket kommer nog att kräva en hel bok
																för att få plats. Alltså är det i princip omöjligt att lyckas få med
																den här på vår hemsida i sin helhet. Vid några tillfällen har vår
																märkliga resa blivit omskriven i olika tidningar och därför väljer
																vi att återge en av artiklarna här för att du ska få en liten glimt
																av allt som hänt. Kommer du på besök berättar vi gärna med våra egna
																ord om alla märkliga sammanträffanden och mirakler som skett men här
																kommer ett litet smakprov ur tidningen Dagen 25 augusti 2020. Den
																fina texten är skriven av Gabriella Mellergårdh och återgiven med
																hennes tillåtelse.
															</p>

															<h4>Deras husbyggardröm blev en berättelse om Guds storhet</h4>
															<p>
																”Bibeln berättar om hur lärjungen Petrus, fylld av tro på Guds
																kraft, klev över båtkanten och började gå över vattnet för att möta
																Jesus. Samma starka tro fick Noa att bygga en jättelik båt på torra
																land. Lenette och Sigge Ahnstedt har påbörjat en helt annan, men
																ändå liknande resa – i tro.
															</p>
															<p>
																Hon gillar att planera och att ha kontroll, något som hon under den
																här resans gång har insett att hon måste släppa, för drömmen om
																Hagablänket ritas om hela tiden. För både Lenette och Sigge är det
																tydligt att den här platsen i grund och botten inte är deras. Den
																tillhör Gud. Och precis som det också står i Bibeln, konstaterar
																Lenette, så är Guds planer många gånger högre och större än våra
																egna. För hur kan man annars förklara att Lenette, frilansflorist
																och musiker, kan rita två stora tvåvåningshus som i dag står
																uppbyggda på platsen, samt ett tredje hus – kapellet – som är på
																gång? Att helt okända människor tar kontakt och blir viktiga
																pusselbitar för allt ifrån markberedning till finansiering? Och att
																en familj med endast en fast inkomst och utan egen byggerfarenhet
																kunnat landa ett projekt som Hagablänket så här långt? – Det vill
																till ett mirakel för att det ska gå. Vi står med skulder och akuta
																räkningar, inte minst efter sommarens avbokningar på grund av
																coronapandemin, men vi vet att Gud har resurserna, säger Lenette.
															</p>
															<p>
																Så låt oss försöka ta historien från början, om hur Lenette och
																Sigge för drygt tio år sedan började planera och drömma, men hur
																kampen om strandskyddsdispens drog ut på tiden, tillstånden uteblev,
																tvivlen växte, landarealen blev mindre än de hade tänkt när marken
																till slut hade styckats av och denna tärande väntan gjorde att
																Lenette till slut gick in i väggen. Åren gick, ändå kunde hon inte
																låta bli att skissa på ritning efter ritning. – Jag kände till sist
																att vi var tvungna att lägga ner alla byggplaner och göra ett
																tydligt avslut för jag slutade ju aldrig att rita hus! Lenette
																skrattar. Hon sa till Gud att ”det enda som kan få mig att ändra mig
																och fortsätta, är om någon ringer och säger att han har mitt hus”,
																och med den kommentaren begravde de visionen. Samtidigt malde ett
																bibelord inom Lenette: ”När tiden var inne att något skulle ske var
																jag där.” (Jesaja 48:16). Och när hennes bror, som höll på att
																avverka i området, undrade om han skulle ta ner lite skog vid sjön
																också, ”ifall era barn vill bygga hus någon gång i framtiden” sa
																Lenette okej. – Plötsligt fanns där bara ett kalhygge. Vi grät, både
																jag och barnen. Skulle jag inte ens kunna åka till vår badplats utan
																att se det där monumentet för vårt misslyckande? säger Lenette.
															</p>
															<p>
																På en av ICCC:s, Kristna Handelskammarens, företagarfrukostar
																berättade hon om drömmen som gått i kras men fick då ett oväntat och
																ganska oönskat svar: ”Det är klart att ni ska bygga! Det är ju bara
																du som är så fylld av fruktan.” – Frågorna hopade sig. Hur skulle
																jag orka? Och var skulle vi få pengar ifrån med bara en fast
																inkomst? Och, kanske den allra största frågan: Varför hade vi fått
																vänta så länge? Lenette och Sigge fick förbön och man skickade med
																dem ett bibelord från Jesaja.
															</p>
															<p>
																Samma kväll satt Lenette och bläddrade i sin egen bibel för att
																hitta bibelordet. Hon hittade inte precis det hon sökte, men hon
																fann något annat. – Plötsligt svarade Gud, sida upp och sida ner på
																alla frågor vi haft. ”Frukta inte.” ”Ett brutet strå ska jag inte
																krossa och en tynande veke ska jag inte släcka.” ”Jag ska ge er
																dolda skatter och bortglömda rikedomar för att ni ska veta att jag
																är Herren.” För varje sida kom det någon ny käftsmäll, och jag blev
																mest irriterad. Lenette ler. Läsningen ur Jesaja fortsatte: Jag har
																förutsagt detta för längesedan, men för att ni inte ska tro at det
																är era egna gudabilder som gjort det, har jag låtit er vänta. Men nu
																är tiden inne, nu ska detta ske som jag sedan länge har förutsagt. –
																Och jag sa till Sigge att, det verkar ju som att Gud vill att vi ska
																bygga hus i alla fall!
															</p>
															<p>
																Dagen därpå när familjen sitter hemma och tittar på tevegudstjänsten
																så ringer telefonen: ”Hej, jag heter Jimmy. Behöver du en
																husstomme?” Det visar sig att denne Jimmy hade en husstomme till
																salu som nästan exakt motsvarade ett av de hus som Lenette ritat.
																Märkligt nog det hus som var så vågat och galet tilltaget att hon
																redan från början sagt till sig själv att ”detta huset kommer vi i
																alla fall aldrig att bygga.” – Gud har sådan humor! Jimmy står på
																sig men Lenette säger nej, gång på gång, för de hade ju lagt ner
																sina planer.
															</p>
															<p>
																Några dagar senare, tre veckor innan semestern 2016, ringer en
																snickare och frågar: Ska ni bygga hus i sommar? Nej, sa Lenette och
																Sigge, igen. Vad synd, svarade snickaren, för annars hade jag kunnat
																komma och gjuta en platta innan semestern. Här kom vändpunkten. – Vi
																kände att vi hade två val. Antingen säger vi nej och får aldrig veta
																vad Gud har tänkt med den här platsen. Eller också säger vi ja, tar
																steget över relingen och börjar gå på vatten. Med bävande hjärtan sa
																Lenette och Sigge ja. Och här sjösattes projekt Hagablänket, som
																efter lång väntan växlade upp i enorm hastighet. Beviljat bygglov
																gällde fyra små stugor, inte ett stort tvåvåningshus på 180
																kvadratmeter, så här gällde att söka nytt. Lenette sprang runt med
																en handritad skiss på huset och fick grannarnas underskrifter. –
																Fyra dagar senare satt vi i byggmöte med kommunen och fick bygglovet
																med oss.
															</p>

															<p>
																Och så har det fortsatt. Varken Lenette eller Sigge hade någon aning
																om vad som krävdes praktiskt men detalj efter detalj har fallit på
																plats genom smått mirakulösa händelser och okända människor som de
																fått kontakt med i precis rätt ögonblick. När leveransen av
																husstommen dröjde kände Lenette hur symptomen från utbrändheten
																gjorde sig påminda igen. Hon bad Gud om ett tydligt tecken och
																svaret kom helt oväntat på en pensionärsträff där Lenette och
																dottern skulle sjunga. En äldre man gav en profetisk hälsning: ”Det
																var så konstigt, när ni sjöng såg jag en bild på ett stort, stort
																hus och en massa människor så var välsignade i vad ni nu håller på
																med!” – Varje gång vi har tvivlat och undrat vad vi håller på med så
																går jag tillbaka till den här punkten, i november 2016, när Gud så
																tydligt talade till oss: Jag är med er i detta, ni ska fortsätta gå.
															</p>

															<p>
																I december 2016 kom så husstommen äntligen på plats och sommaren
																2017 invigdes bottenvåningen på Skogslugnet i Hagablänket med de
																första bokade gästerna, efter ett halvårs snickeriarbete med Lenette
																som byggledare. Den allra första retreaten i huset gick av stapeln
																inte långt därefter, helt enligt Lenettes dröm men väldigt mycket
																tidigare än hon själv hade planerat. – Det är otroligt hur Gud
																jobbar, han sparkar in en i grejer som man inte tror att man är
																mogen för. Huset var inte färdigbyggt, jag var inte färdigtänkt, men
																sedan dess har vi haft tre retreater om året i Missionsförsamlingens
																regi och det har varit helt fantastiska helger. Huset är som klippt
																och skuret för det här, säger Lenette.
															</p>

															<p>
																Sedan dess har det fortsatt i högt tempo. Övervåningen
																färdigställdes våren 2018 och i fjol var huset uthyrt hela sommaren.
																Då förbereddes också plats till både ett kapell och ett garage – som
																i slutändan visade sig bli inte bara ett garage utan ännu ett
																tvåvåningshus för uthyrning. – Jag började rita ett garage men fick
																inte till det, så jag bad vårt bärarlag om förbön. De bad att Gud
																skulle ge mig mönsterbilden för nästa hus i Hagablänket, att Gud
																skulle hålla i pennan, och så blev det. Huset var färdigritat på en
																kvart, berättar Lenette. Det var den 22 augusti 2019. Därefter
																följde märkliga möten med pingstvänner och Tanzaniska evangelister
																på rastplatsen Höganloft i Tranås. En husförsäljare blev oväntat
																berörd av visionen bakom Hagablänket och gick själv in för att
																hjälpa Lenette och Sigge – och den 13 mars 2020 levererades stommen.
																– Redan den 25 maj, bara drygt två månader senare, var det dags för
																slutbesiktning av Sjömagasinet.
															</p>

															<p>
																– Det verkar som att Gud har väldigt bråttom med att få klart det
																här stället. Precis när vi tror att vi kan andas ut så smäller det
																till igen, säger Sigge och pekar upp mot kapellplatsen där virke
																ligger och väntar på byggstart. – Kanske är det meningen att det ska
																gå så här snabbt för att människor ska förstå att vi inte gör det
																här av egen kraft. Framöver ska Lenette och Sigge också hålla sin
																första äktenskapsretreat tillsammans. – Det är några par som har
																sagt att de vill komma. De vet att vi aldrig har gjort det här
																förut, men de har sagt att vi får öva på dem, så nu är vi här,
																utanför båtkanten igen, säger Lenette Ahnstedt och skrattar.”
															</p>
														</article>
													</section>
												</div>
											</div>
										</div>
									{/if}
								</svelte:fragment>
							</TabGroup>
						</div>
					</section>

					<section>
						<div class="card p-4 px-10">
							<div class="max-w-screen-xl px-4 py-8 mx-auto sm:py-12 sm:px-6 lg:px-8">
								<div class="grid grid-cols-1 gap-4 lg:grid-cols-2 lg:items-stretch">
									<div class="grid p-6 rounded place-content-center sm:p-8">
										<div class="max-w-md mx-auto text-center lg:text-left">
											<header>
												<h2 class="text-xl font-bold sm:text-3xl">Stöd oss</h2>
											</header>

											<article class="space-y-4 pt-4">
												<p>
													Hagablänket är inte i första hand uppbyggt för kommersiell uthyrning. Vi
													tror att det ska vara ett ställe där människor i olika åldrar kan få landa
													och hämta kraft. En plats för upprättelse, helande och växande på olika
													sätt. Vår bön är att Hagablänket ska vara en plats där människor får känna
													Guds frid och ges möjlighet att komma närmare Jesus Kristus som själv
													säger: Jag är vägen, sanningen och livet. Ingen kommer till Fadern (Gud)
													utom genom mig.
												</p>

												<p>
													För att detta ska kunna bli verklighet är vi helt beroende av hjälp från
													olika håll. Du kan stödja oss på olika sätt genom månadsgivande,
													engångsgåvor, dina förböner, sponsring av annonser eller olika typer av
													praktisk hjälp eller volontärtjänst. Kontakta oss för mer information, vi
													är så tacksamma för allt stöd vi kan få!
												</p>
											</article>

											<article class="pt-4 space-y-2">
												<p>Svenskt Bankgiro: 549-1709</p>

												<p>Swish: 123 322 96 14</p>

												<p>Märk insättningen med ”Gåva”</p>
											</article>

											<article class="pt-4 space-y-1">
												<p>Internationella gåvor:</p>

												<p>Mottagarnamn: Lenette Ahnstedt Axebo, Farstorpsvägen 12, 574 98 Nye</p>

												<p>
													IBAN (international bank account number): SE21 8000 0840 5333 3874 9561
												</p>

												<p>BIC (bank identifier code): SWEDSESS</p>

												<p>Bankens adress: Virserums Sparbank, Storgatan 8, 577 71 Virserum</p>
											</article>

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
