<script>
	export let segment
</script>

<style>
	ul {
		display: flex;
		list-style: none;
		margin: 0;
	}

	li:not(:last-child) {
		margin-right: 1rem;
	}
</style>

<nav>
	<ul>
		<li>
			<a class:selected='{segment === "resume"}' href="/project?p=resume">Resume</a>
		</li>
	</ul>
	<!-- <ul>
		<li><a class:selected='{segment === undefined}' href='.'>home</a></li>
		<li><a class:selected='{segment === "about"}' href='about'>about</a></li>

		for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen
		<li><a rel=prefetch class:selected='{segment === "blog"}' href='blog'>blog</a></li>
	</ul> -->
</nav>
