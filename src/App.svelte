<script>
	import {onMount} from "svelte";
    import { Router, Route } from './components/svero/main';
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


<Router nofallback  >

  <Route fallback path="*"><Home /></Route>
  <Route path="#publicEducation">
    <PublicEducation />
  </Route>

  <Route path="#EventRequest">
    <PubEventForm />
  </Route>

  
</Router>



<Footer />


