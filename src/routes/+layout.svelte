<script>
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import Header from '$lib/Header.svelte';

	import '../app.css';
	import { page } from '$app/state';
	import Footer from '$lib/Footer.svelte';

	let { children } = $props();

	const stuff = {
		title: `Marci Metzger Homes - Real Estate Agent, Real Estate, Realtor`,
		desc: `Marci Metzger Homes - Pahrump, NV - Over two decades in real estate. Licensed Broker in Seattle, now serving Southern Nevada as Pahrump's top real estate agent.`,
		image: `https://img1.wsimg.com/isteam/ip/067a4d42-19e8-46d9-9bed-578bf62dd44e/mtn%20falls%20pond.jpg`
	};
	let url = $derived(page.url);
</script>

<svelte:head>
	<title>{stuff?.title}</title>
	<meta name="robots" content="index, follow" />
	<meta name="description" content={stuff?.desc} />
	<meta property="og:locale" content="en_US" />
	<meta property="og:type" content="website" />
	<meta property="og:title" content={stuff?.title} />
	<meta property="og:description" content={stuff?.desc} />
	<meta property="og:url" content="https://marcimetzger.com/" />
	<meta property="og:site_name" content="Marci Metzger Homes" />
	<meta property="og:image" content={stuff?.image} />
	<meta property="og:image:width" content="800" />
	<meta property="og:image:height" content="450" />
	<meta property="og:image:type" content="image/jpeg" />

	<link rel="canonical" href={url} />
	<link rel="icon" href={favicon} />
</svelte:head>

<Header />
{@render children?.()}
<Footer />
