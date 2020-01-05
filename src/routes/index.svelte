<script>
	import Projects from '../components/Projects.svelte';
</script>
<style>
	#introduction {
		text-align: center;
	}
	#introduction > h1 {
		font-size: 2rem;
		color: #38b8ff;
	}
	#introduction > p {
		font-size: 1.75rem;
	}
	.strike {
		text-decoration: line-through;
	}
</style>

<section id="introduction">
	<h1>
		Hello, I am Raviteja Puppala.
	</h1>
	<p>
		I Create Better Experiences For <span class="strike">Users</span> People
	</p>
</section>

<Projects />
