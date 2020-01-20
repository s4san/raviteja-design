<script>
    import Testimonials from './Testimonials.svelte'
    export let segment;
</script>
<footer>
    {#if segment === undefined}
        <Testimonials />
    {/if}
    <nav>
        <ul>
            <li>
                <a href="https://dribbble.com/Ravitejapuppala" rel="nofollow noopener" title="Dribbble profile">
                    <img src="dribbble.svg" alt="Dribbble">
                </a>
            </li>
            <li>
                <a href="https://www.linkedin.com/in/ravitejapuppala/" rel="nofollow noopener" title="LinkedIn Profile">
                    <img src="linkedin.svg" alt="LinkedIn">
                </a>
            </li>
            <li>
                <a href="https://twitter.com/Ravytez" rel="nofollow noopener" title="Twitter Profile">
                    <img src="twitter.svg" alt="Twitter">
                </a>
            </li>
            <li>
                <a href="https://www.instagram.com/ravy_tezz/" rel="nofollow noopener" title="Instagram Profile">
                    <img src="instagram.svg" alt="Instagram">
                </a>
            </li>
        </ul>
    </nav>
    <p>
        Made with ❤ by Raviteja and @asyncloop
    </p>
</footer>
<style>
    footer {
        background-color: #0d48a2;
        color: #FFF;
        min-height: 12rem;
        padding: 4rem 1rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        clip-path: polygon(
            0 0,
            100% 10%,
            100% 100%,
            0 100%
        );
    }

    footer > * {
        width: 70vw;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    ul {
        margin: 0;
        padding: 0;
        display: flex;
        list-style: none;
    }

    li {
        margin: 0 1rem;
    }

    a,
    a:hover,
    a:active,
    a:focus {
        text-decoration: none;
    }

    a > img {
        width: 2rem;
        height: 2rem;
    }

    p {
        margin-bottom: 0;
    }
</style>
