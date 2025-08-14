<script>
	import { onMount, onDestroy } from 'svelte';

	let currentSlide = 0;
	let autoplay = true;
	let interval;

	const slides = [
		{
			title: 'Discover New Horizons',
			description: 'Travel experiences that will change your life',
			buttonText: 'Book Now',
			buttonUrl: '#',
			image: '/carousel1.webp'
		},
		{
			title: 'Natural Wonders',
			description: 'Breathtaking views and unspoiled nature',
			buttonText: 'View Offers',
			buttonUrl: '#',
			image: '/carousel2.webp'
		},
		{
			title: 'Urban Adventure',
			description: 'Modern cities full of life and culture',
			buttonText: 'Learn More',
			buttonUrl: '#',
			image: '/carousel3.webp'
		},
		{
			title: 'Discover New Horizons',
			description: 'Travel experiences that will change your life',
			buttonText: 'Book Now',
			buttonUrl: '#',
			image: '/carousel4.webp'
		},
		{
			title: 'Natural Wonders',
			description: 'Breathtaking views and unspoiled nature',
			buttonText: 'View Offers',
			buttonUrl: '#',
			image: '/carousel5.webp'
		},
		{
			title: 'Urban Adventure',
			description: 'Modern cities full of life and culture',
			buttonText: 'Learn More',
			buttonUrl: '#',
			image: '/carousel6.webp'
		},
		{
			title: 'Urban Adventure',
			description: 'Modern cities full of life and culture',
			buttonText: 'Learn More',
			buttonUrl: '#',
			image: '/carousel7.webp'
		}
	];

	function next() {
		currentSlide = (currentSlide + 1) % slides.length;
	}

	function prev() {
		currentSlide = (currentSlide - 1 + slides.length) % slides.length;
	}

	function goTo(index) {
		currentSlide = index;
	}

	function startAutoplay() {
		interval = setInterval(() => {
			if (autoplay) {
				next();
			}
		}, 5000);
	}

	function replaceBrokenImage(event) {
		const fallbacks = [
			'https://picsum.photos/id/1018/1920/1080',
			'https://picsum.photos/id/1015/1920/1080',
			'https://picsum.photos/id/1019/1920/1080'
		];
		event.target.src = fallbacks[currentSlide % fallbacks.length];
	}

	onMount(() => {
		startAutoplay();
	});

	onDestroy(() => {
		clearInterval(interval);
	});
</script>

<div
	class="relative overflow-hidden"
	on:mouseenter={() => (autoplay = false)}
	on:mouseleave={() => (autoplay = true)}
	role="button"
	tabindex="-1"
>
	<div class="relative h-[80vh] min-h-[500px]">
		{#each slides as slide, index}
			{#if currentSlide === index}
				<div class="hero-slide absolute inset-0">
					<div class="absolute inset-0 bg-gray-800">
						<img
							src={slide.image}
							alt={slide.title}
							class="h-full w-full object-cover"
							on:error={replaceBrokenImage}
							loading="lazy"
						/>
					</div>

					<div class="container mx-auto flex h-full items-end px-6 py-8">
						<div
							class="slide-content max-w-2xl text-white"
							class:translate-x-0={currentSlide === index}
							class:opacity-100={currentSlide === index}
							class:translate-x-10={currentSlide !== index}
							class:opacity-0={currentSlide !== index}
						>
							<h2
								class="mb-4 text-4xl font-bold md:text-5xl"
								style="text-shadow: 2px 2px 4px rgba(0,0,0,0.4);"
							>
								{slide.title}
							</h2>
							<p class="mb-6 text-xl md:text-2xl" style="text-shadow: 2px 2px 4px rgba(0,0,0,0.3);">
								{slide.description}
							</p>
							<a
								href={slide.buttonUrl}
								class="fade-in inline-block rounded-lg bg-blue-600 px-8 py-3 text-lg font-semibold text-white transition-colors hover:bg-blue-700"
							>
								{slide.buttonText}
							</a>
						</div>
					</div>
				</div>
			{/if}
		{/each}

		<!-- Prev Button -->
		<button
			on:click={prev}
			class="absolute top-1/2 left-4 z-10 flex h-10 w-10 -translate-y-1/2 items-center justify-center rounded-full bg-black/50 text-white transition-all hover:bg-black/70 md:h-12 md:w-12"
			aria-label="Previous slide"
		>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				class="h-5 w-5 md:h-6 md:w-6"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
			>
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
			</svg>
		</button>

		<!-- Next Button -->
		<button
			on:click={next}
			class="absolute top-1/2 right-4 z-10 flex h-10 w-10 -translate-y-1/2 items-center justify-center rounded-full bg-black/50 text-white transition-all hover:bg-black/70 md:h-12 md:w-12"
			aria-label="Next slide"
		>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				class="h-5 w-5 md:h-6 md:w-6"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
			>
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
			</svg>
		</button>

		<!-- Dots -->
		<div class="absolute bottom-8 left-1/2 z-10 flex -translate-x-1/2 space-x-2">
			{#each slides as _, index}
				<button
					on:click={() => goTo(index)}
					class="h-2 w-2 rounded-full transition-all md:h-3 md:w-3"
					class:bg-white={currentSlide === index}
					class:w-4={currentSlide === index}
					class:md\:w-6={currentSlide === index}
					class:bg-white\50={currentSlide !== index}
					aria-label={`Go to slide ${index + 1}`}
				></button>
			{/each}
		</div>
	</div>
</div>

<style>
	.hero-slide {
		transition:
			opacity 0.8s ease,
			transform 0.8s ease;
	}
	.slide-content {
		transition: all 0.6s ease 0.3s;
	}
	.fade-in {
		animation: fadeIn 1s ease-in;
	}
	@keyframes fadeIn {
		from {
			opacity: 0;
		}
		to {
			opacity: 1;
		}
	}
</style>
