<body>
	<div class="px-4 py-2">
		<ol class="breadcrumb">
			<li class="crumb">Home</li>
			<li class="crumb-separator" aria-hidden>/</li>
			<li>Menu</li>
		</ol>
	</div>

	<div class="container px-10 py-7 space-y-6">
		<h2>Menu</h2>
	</div>

	<div class="px-8 pd-4">
		<div class="rounded-md drop-shadow-[0_1.2px_6.2px_rgba(0,0,0,0.8)] bg-white">
			<div
				class="mx-auto grid max-w-2xl grid-cols-1 items-center gap-x-8 gap-y-16 px-4 md:py-16 lg:py-16 sm:px-6 sm:py-32 lg:max-w-7xl lg:grid-cols-2 lg:px-8"
			>
				<div class="py-2">
					<h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
						The Chef of the Season
					</h2>
					<p class="mt-4 text-gray-800">
						The Iron Chef is honored to be led this summer season by non other then The Gordon
						Ramsey, and we can guarantee that Menu and the experience you will have with us is
						something you won't forget soon.
					</p>

					<dl class="mt-16 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 sm:gap-y-16 lg:gap-x-8">
						<div class="border-t border-gray-200 pt-4">
							<dt class="font-medium text-gray-900">Origin</dt>
							<dd class="mt-2 text-sm text-gray-800">
								All of our engedients are imported from the country of origin and if not possible
								carefully replaced with high end ingredients
							</dd>
						</div>
						<div class="border-t border-gray-200 pt-4">
							<dt class="font-medium text-gray-900">Base Menu</dt>
							<dd class="mt-2 text-sm text-gray-800">
								Solid and timeless, we always have these at hand
							</dd>
						</div>
						<div class="border-t border-gray-200 pt-4">
							<dt class="font-medium text-gray-900">Lunch or Dinner?</dt>
							<dd class="mt-2 text-sm text-gray-800">
								We have perfectly tailored the menu and price to fit the season as well as your
								wallet
							</dd>
						</div>
						<div class="border-t border-gray-200 pt-4">
							<dt class="font-medium text-gray-900">From abroad</dt>
							<dd class="mt-2 text-sm text-gray-800">
								With our specials we are always lead by a chef from the country of origin to ensure
								quality and the authenticity
							</dd>
						</div>
					</dl>
					<div class="pt-8">
						<p class="mt-4 text-black">
							Check out the menu here!
							<a
								href="https://thebarn.se/wp-content/uploads/2023/05/The_Barn_Allehanda_2023-webb.pdf"
								>https://thebarn.se/wp-content/uploads/2023/05/The_Barn_Allehanda_2023-webb.pdf</a
							>
							<br />
							<br />
							Gordon is also part of our Cooking Lessons, check out this free lesson!
						</p>
						<div class="pt-2">
							<iframe
								width="560"
								height="315"
								src="https://www.youtube.com/embed/ulhRORJpuBM"
								title="YouTube video player"
								frameborder="0"
								allowfullscreen
							/>
						</div>
					</div>
				</div>
				<div class="flex justify-end px-4">
					<img
						src="https://parade.com/.image/t_share/MTkyMzM2MjcwMzU2MTk0NTQ2/gordon-ramsay-restaurants.jpg"
						alt="Gordon Ramsey posing."
						class="rounded-lg text-white bg-gray-100"
					/>
				</div>
			</div>
		</div>
	</div>
	<slot />
	<!-- ---- / ---- -->
</body>
