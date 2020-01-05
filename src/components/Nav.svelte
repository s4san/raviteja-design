<script>
	export let segment;
</script>

<style>
	ul {
		display: flex;
		list-style: none;
	}

	li:not(:last-child) {
		margin-right: 16px;
	}
</style>

<nav>
	<ul>
		<li>About</li>
		<li>Resume</li>
		<li>Contact</li>
	</ul>
	<!-- <ul>
		<li><a class:selected='{segment === undefined}' href='.'>home</a></li>
		<li><a class:selected='{segment === "about"}' href='about'>about</a></li>

		for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen
		<li><a rel=prefetch class:selected='{segment === "blog"}' href='blog'>blog</a></li>
	</ul> -->
</nav>
