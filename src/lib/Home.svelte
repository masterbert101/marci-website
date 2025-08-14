<script>
	import Carousel from './Carousel.svelte';

	let contents = [
		{
			src: '/contents1.webp',
			title: 'Top Residential Sales Last 5 Years',
			excerpt: `We helped nearly 90 clients in 2021, and closed 28.5 million in sales! Our team works hard everyday to grow and learn, so that we may continue to excel in our market. Our clients deserve our best, & we want to make sure our best is better every year.`
		},
		{
			src: '/contents2.webp',
			title: `Don't Just List it...`,
			excerpt: `Get it SOLD! We exhaust every avenue to ensure our listings are at the fingertips of every possible buyer, getting you top dollar for your home.`
		},
		{
			src: '/contents3.webp',
			title: 'Guide to Buyers',
			excerpt: `Nobody knows the market like we do. Enjoy having a pro at your service. Market analysis, upgrades lists, contractors on speed dial, & more!`
		}
	];
</script>

<section class="relative h-screen" style="background-image: url('/herobg.webp')">
	<div class=" mx-auto max-w-7xl px-4 pt-64 pb-16 text-center sm:px-6 lg:px-8">
		<p class="mx-auto -mt-2 max-w-2xl text-2xl tracking-tight text-white sm:mt-6">
			MARCI METZGER - THE RIDGE REALTY GROUP
		</p>

		<h1
			class="font-display mx-auto max-w-4xl text-5xl font-medium tracking-tight text-white sm:text-8xl"
		>
			<span class="inline-block">
				<span class="relative whitespace-nowrap text-gray-100">
					<svg
						aria-hidden="true"
						viewBox="0 0 418 42"
						class="absolute top-2/3 left-0 h-[0.58em] w-full fill-blue-300/70"
						preserveAspectRatio="none"
						><path
							d="M203.371.916c-26.013-2.078-76.686 1.963-124.73 9.946L67.3 12.749C35.421 18.062 18.2 21.766 6.004 25.934 1.244 27.561.828 27.778.874 28.61c.07 1.214.828 1.121 9.595-1.176 9.072-2.377 17.15-3.92 39.246-7.496C123.565 7.986 157.869 4.492 195.942 5.046c7.461.108 19.25 1.696 19.17 2.582-.107 1.183-7.874 4.31-25.75 10.366-21.992 7.45-35.43 12.534-36.701 13.884-2.173 2.308-.202 4.407 4.442 4.734 2.654.187 3.263.157 15.593-.78 35.401-2.686 57.944-3.488 88.365-3.143 46.327.526 75.721 2.23 130.788 7.584 19.787 1.924 20.814 1.98 24.557 1.332l.066-.011c1.201-.203 1.53-1.825.399-2.335-2.911-1.31-4.893-1.604-22.048-3.261-57.509-5.556-87.871-7.36-132.059-7.842-23.239-.254-33.617-.116-50.627.674-11.629.54-42.371 2.494-46.696 2.967-2.359.259 8.133-3.625 26.504-9.81 23.239-7.825 27.934-10.149 28.304-14.005.417-4.348-3.529-6-16.878-7.066Z"
						></path></svg
					>
					<span class="relative">Pahrump Realtor</span></span
				>
			</span>
		</h1>

		<p class="mx-auto mt-9 max-w-2xl text-xl tracking-tight text-slate-100 sm:mt-6">
			<span class="inline-block"
				>Trusted Pahrump Realtor delivering results with integrity and care.</span
			>
		</p>

		<div
			class="mt-12 flex flex-col justify-center gap-y-5 sm:mt-10 sm:flex-row sm:gap-x-6 sm:gap-y-0"
		>
			<div
				class="relative flex flex-1 flex-col items-stretch sm:flex-none"
				data-headlessui-state=""
			>
				<a
					role="button"
					class="group relative inline-flex items-center justify-center rounded-full bg-white px-8 py-3 text-base font-semibold text-[#147de3] transition-all duration-200 hover:-translate-y-0.5 hover:shadow-lg hover:shadow-gray-600/30"
					title="payment"
					href="#"
					>CALL NOW<svg
						aria-hidden="true"
						viewBox="0 0 10 10"
						height="10"
						width="10"
						fill="none"
						class=" -mr-1 ml-2 stroke-[#147de3] stroke-2"
					>
						<path d="M0 5h7" class="opacity-0 transition group-hover:opacity-100"></path>
						<path d="M1 1l4 4-4 4" class="transition group-hover:translate-x-[3px]"></path>
					</svg>
				</a>
			</div>
		</div>
	</div>

	<div class=" mx-auto hidden max-w-6xl rounded-lg bg-white p-6 shadow-md md:block">
		<h2 class="text-2xl">Find Your Dream Home</h2>
		<h2 class="my-2 text-xl text-gray-700">Search Listings</h2>

		<form class="grid grid-cols-1 gap-4 md:grid-cols-4">
			<!-- Location -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Location</label>
				<select
					class="w-full rounded-md border border-gray-300 px-3 py-2 focus:ring focus:ring-pink-200 focus:outline-none"
				>
					<option value="">Select</option>
				</select>
			</div>

			<!-- Type -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Type</label>
				<select
					class="w-full rounded-md border border-gray-300 px-3 py-2 focus:ring focus:ring-pink-200 focus:outline-none"
				>
					<option value="">Select</option>
				</select>
			</div>

			<!-- Sort By -->
			<div class="md:col-span-2">
				<label class="mb-1 block text-sm text-gray-600">Sort By</label>
				<select
					class="w-full rounded-md border border-gray-300 px-3 py-2 focus:ring focus:ring-pink-200 focus:outline-none"
				>
					<option value="">Select</option>
				</select>
			</div>

			<!-- Bedrooms -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Bedrooms</label>
				<select class="w-full rounded-md border border-gray-300 px-3 py-2">
					<option>Any Number</option>
				</select>
			</div>

			<!-- Baths -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Baths</label>
				<select class="w-full rounded-md border border-gray-300 px-3 py-2">
					<option>Any Number</option>
				</select>
			</div>

			<!-- Min Price -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Min Price</label>
				<input type="number" class="w-full rounded-md border border-gray-300 px-3 py-2" />
			</div>

			<!-- Max Price -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Max Price</label>
				<input type="number" class="w-full rounded-md border border-gray-300 px-3 py-2" />
			</div>

			<!-- Search Button -->
			<div class="flex justify-end md:col-span-4">
				<button
					type="submit"
					class="cursor-not-allowed rounded-full bg-gray-200 px-6 py-3 font-semibold text-gray-500"
					disabled
				>
					Search Now
				</button>
			</div>
		</form>
	</div>
</section>

<section class="p-4">
	<div class="mx-auto block max-w-6xl rounded-lg bg-white p-6 shadow-lg md:hidden">
		<h2 class="text-2xl">Find Your Dream Home</h2>
		<h2 class="my-2 text-xl text-gray-700">Search Listings</h2>

		<form class="grid grid-cols-1 gap-4 md:grid-cols-4">
			<!-- Location -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Location</label>
				<select
					class="w-full rounded-md border border-gray-300 px-3 py-2 focus:ring focus:ring-pink-200 focus:outline-none"
				>
					<option value="">Select</option>
				</select>
			</div>

			<!-- Type -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Type</label>
				<select
					class="w-full rounded-md border border-gray-300 px-3 py-2 focus:ring focus:ring-pink-200 focus:outline-none"
				>
					<option value="">Select</option>
				</select>
			</div>

			<!-- Sort By -->
			<div class="md:col-span-2">
				<label class="mb-1 block text-sm text-gray-600">Sort By</label>
				<select
					class="w-full rounded-md border border-gray-300 px-3 py-2 focus:ring focus:ring-pink-200 focus:outline-none"
				>
					<option value="">Select</option>
				</select>
			</div>

			<!-- Bedrooms -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Bedrooms</label>
				<select class="w-full rounded-md border border-gray-300 px-3 py-2">
					<option>Any Number</option>
				</select>
			</div>

			<!-- Baths -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Baths</label>
				<select class="w-full rounded-md border border-gray-300 px-3 py-2">
					<option>Any Number</option>
				</select>
			</div>

			<!-- Min Price -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Min Price</label>
				<input type="number" class="w-full rounded-md border border-gray-300 px-3 py-2" />
			</div>

			<!-- Max Price -->
			<div>
				<label class="mb-1 block text-sm text-gray-600">Max Price</label>
				<input type="number" class="w-full rounded-md border border-gray-300 px-3 py-2" />
			</div>

			<!-- Search Button -->
			<div class="flex justify-end md:col-span-4">
				<button
					type="submit"
					class="cursor-not-allowed rounded-full bg-gray-200 px-6 py-3 font-semibold text-gray-500"
					disabled
				>
					Search Now
				</button>
			</div>
		</form>
	</div>
</section>

<section class="md:pt-30">
	<div
		class="mx-auto grid max-w-7xl grid-cols-2 justify-items-center gap-y-8 px-4 py-10 md:flex md:justify-between md:gap-y-0 md:pt-20"
	>
		<img src="ridge.webp" alt="ridge" />
		<img src="equal.webp" alt="equal" />
		<img src="realtor.webp" alt="realtor" />
		<img src="pahrump.webp" alt="pahrump" />
	</div>
</section>

<section class="px-4 pt-4">
	<div class="mx-auto grid max-w-5xl items-center justify-center gap-y-8 md:gap-y-0 lg:flex">
		<div class="order-2 h-full text-center md:order-1">
			<h1 class="text-3xl font-bold text-[#147de3] md:text-[86px]">MARCI METZGER</h1>
			<p class="my-2 text-lg leading-[50px] font-medium text-gray-600 md:text-2xl">
				REALTOR FOR NEARLY 3 DECADES!
			</p>
			<p class="m-0 text-3xl leading-[25px] font-medium text-gray-600 md:my-2 md:leading-[50px]">
				206-919-6886
			</p>
		</div>
		<img
			class="order-1 rounded-full shadow-lg md:order-2 md:h-[470px] md:w-[470px]"
			src="/marci.webp"
			alt="marci"
		/>
	</div>
</section>

<section class="mx-auto grid max-w-7xl gap-4 px-4 py-10 md:gap-8 md:px-12 md:py-16">
	<div class="w-full text-center">
		<div class="clients-text-wrapper">
			<h2 class="my-2 text-2xl font-bold text-gray-700 md:text-3xl">GET IT SOLD</h2>
			<p class="mx-auto mt-2 max-w-4xl text-lg font-medium text-gray-500">
				With over $28.5M in sales in 2021, our team goes beyond just listing — we get your home
				SOLD, reaching every possible buyer to secure top dollar.
			</p>
		</div>
	</div>

	<ul class="grid gap-8 md:grid-cols-3">
		{#each contents as n}
			<li class="overflow-hidden rounded-2xl bg-white shadow-md/50">
				<div>
					<button class="m-0 p-0 outline-none" onclick={() => (showModal = true)}>
						<img
							class="block w-full object-cover"
							src={n.src}
							alt={n.title}
							width="350"
							height="350"
						/>
					</button>
				</div>
				<div class="p-4">
					<h3 class="text-xl text-gray-800">{n.title}</h3>
					{#if n.excerpt}
						<p class="mt-1 text-sm text-gray-600">{n.excerpt}</p>
					{/if}
				</div>
			</li>
		{/each}
	</ul>
</section>

<section>
	<Carousel />
</section>

<section class="mx-auto w-full bg-gray-50 py-8 md:py-10 dark:text-white">
	<div class="clients-text-wrapper text-center">
		<h2 class="text-2xl font-bold text-gray-700 md:my-2 md:text-3xl">OUR SERVICES</h2>
	</div>

	<div class="flex h-full w-full flex-col items-center py-6 md:py-4 md:py-10">
		<div
			class="mx-auto mt-4 flex w-[90%] flex-col justify-center gap-2 sm:w-[85%] md:flex-row md:items-center lg:items-stretch lg:gap-4 xl:w-[80%]"
		>
			<img
				class="w-full rounded-sm md:w-[50%] md:rounded-t-lg"
				src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w0NzEyNjZ8MHwxfHNlYXJjaHw1fHxob21lfGVufDB8MHx8fDE3MTA0OTAwNjl8MA&ixlib=rb-4.0.3&q=80&w=1080"
				alt="billboard image"
			/>

			<div
				class="flex w-full flex-col justify-center rounded-md p-0 md:w-[50%] md:bg-gray-100 md:p-4 dark:text-gray-400"
			>
				<h2 class="pt-4 text-3xl font-semibold text-gray-900 dark:text-gray-700">
					Real Estate Done Right
				</h2>
				<p class="text-md mt-4">
					Nervous about your property adventure? Don’t be. Whether you're getting ready to buy or
					sell your residence, looking at investment properties, or just curious about the markets,
					our team ensures you get the best experience possible!
				</p>
			</div>
		</div>

		<div
			class="mx-auto mt-4 grid w-[90%] flex-col justify-center gap-2 sm:w-[85%] md:flex md:flex-row md:items-center lg:items-stretch lg:gap-4 xl:w-[80%]"
		>
			<div
				class="order-2 flex w-full flex-col justify-center rounded-md p-0 md:order-1 md:w-[50%] md:bg-gray-100 md:p-4 dark:text-gray-400"
			>
				<h2 class="pt-4 text-3xl font-semibold text-gray-900">Commercial & Residential</h2>
				<p class="text-md mt-4">
					Large or small, condo or mansion, we can find it and get at the price that's right.
					Fixer-uppers? Luxury? We can help with all of it! We live, work, and play in this
					community. Happy to help you find where to put you hard-earned dollars.
				</p>
			</div>

			<img
				class="order-1 w-full rounded-sm md:order-2 md:w-[50%] md:rounded-t-lg"
				src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w0NzEyNjZ8MHwxfHNlYXJjaHw1fHxob21lfGVufDB8MHx8fDE3MTA0OTAwNjl8MA&ixlib=rb-4.0.3&q=80&w=1080"
				alt="billboard image"
			/>
		</div>

		<div
			class="mx-auto mt-4 flex w-[90%] flex-col justify-center gap-2 sm:w-[85%] md:flex-row md:items-center lg:items-stretch lg:gap-4 xl:w-[80%]"
		>
			<img
				class="w-full rounded-sm md:w-[50%] md:rounded-t-lg"
				src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w0NzEyNjZ8MHwxfHNlYXJjaHw1fHxob21lfGVufDB8MHx8fDE3MTA0OTAwNjl8MA&ixlib=rb-4.0.3&q=80&w=1080"
				alt="billboard image"
			/>

			<div
				class="flex w-full flex-col justify-center rounded-md p-0 md:w-[50%] md:bg-gray-100 md:p-4 dark:text-gray-400"
			>
				<h2 class="pt-4 text-3xl font-semibold text-gray-900 dark:text-gray-700">
					Real Estate Done Right
				</h2>
				<p class="text-md mt-4">
					Nervous about your property adventure? Don’t be. Whether you're getting ready to buy or
					sell your residence, looking at investment properties, or just curious about the markets,
					our team ensures you get the best experience possible!
				</p>
			</div>
		</div>
	</div>
</section>
