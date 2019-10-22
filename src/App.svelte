<script>
	import Splash from './pages/Splash.svelte';
	import Header from './components/Header.svelte';
	import Home from './pages/Home.svelte';
	import PublicEducation from './pages/PublicEducation.svelte';
	import PubEventForm from './pages/PubEventForm.svelte';
	 import Footer from './components/Footer.svelte';
	import { fade } from 'svelte/transition';
	let splash = true;
	setTimeout(() => {
		splash = false;
	}, 500);

	function handleURL() {
		
	}
</script>

<Header />
<!-- <Home /> -->
<PublicEducation />
<!-- <PubEventForm /> -->

<Footer />


