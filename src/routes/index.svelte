<script>
	import Projects from '../components/Projects.svelte';
</script>
<style>
	section {
		text-align: center;
	}

	section > p {
		font-size: 1.75rem;
	}

	.strike {
		text-decoration: line-through;
	}

	.decorative {
		font-family: fantasy;
		color: #ffc10c;
	}
</style>

<section id="introduction">
	<h1>
		Hello, I am Raviteja Puppala.
	</h1>
	<p>
		I Create Better Experiences For
		<span class="strike">Users</span>
		<span class="decorative"> People</span>
	</p>
</section>

<Projects />
