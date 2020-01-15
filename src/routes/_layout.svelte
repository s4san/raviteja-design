<script>
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte';

	export let segment;
</script>

<style>
	header, main {
		background: #FFF;
		margin-right: 4rem;
		margin-left: 1.5rem;
	}

	header {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	h2 {
		font-size: 1.25rem;
	}
</style>

<svelte:head>
	<title>Raviteja Puppala</title>
</svelte:head>

<header>
	<a href="/">
		<h2>Home</h2>
	</a>
	<Nav/>
</header>
<main>
	<slot></slot>
</main>
<Footer {segment}/>
