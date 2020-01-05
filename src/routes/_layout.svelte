<script>
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte';

	export let segment;
</script>

<style>
	header, main {
		background: #FFF;
	}

	header {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
</style>

<svelte:head>
	<title>Raviteja Puppala</title>
</svelte:head>

<header>
	<h2>Raviteja Puppala</h2>
	<Nav {segment}/>
</header>
<main>
	<slot></slot>
</main>
<Footer />
