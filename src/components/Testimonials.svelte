<script>
    import Carousel from './Carousel.svelte';
    import Testimonial from './Testimonial.svelte';
    export let testimonials = [
        {
            name: 'Greg Morgan',
            title: 'Co-founder & CEO, Zoomcar',
            content: 'Ravi is a high energy individual who was a high impact contributor from his earliest days at Zoomcar. He always took initiative and was eager to learn new skills and approaches to design as his tenure evolved. He was also a great team player'
        }
    ];
</script>
<section>
	<h2>
		People who trust me with their hearts
	</h2>
    <Carousel>
        {#each testimonials as { name, title, content }}
            <Testimonial {name} {title} {content} />
        {/each}
    </Carousel>
    <p>* Recommendations given on LinkedIn</p>
</section>
<style>
    h2 {
        text-align: center;
        font-size: 1.5rem;
        margin-bottom: 3rem;
    }
    p {
        margin: 1.5rem 0 3rem 0;
        font-size: 0.75rem;
        opacity: 0.41;
        text-align: center;
    }
</style>
