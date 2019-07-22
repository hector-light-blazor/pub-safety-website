<script>
	import Splash from './pages/Splash.svelte';
	import Home from './pages/Home.svelte';
	import PubEvent from './pages/PubEvent.svelte';
	import { fade } from 'svelte/transition';
	let splash = true;
	setTimeout(() => {
		splash = false;
	}, 500);
</script>


  <!-- <Home /> -->
<PubEvent />

