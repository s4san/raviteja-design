<section>
    <a href="/project?p=lmd">
        <figure>
            <img src="lmd-logo.svg" alt="LMD Logo">
            <div class="bg-only"></div>
            <figcaption>Last Mile Delivery</figcaption>
        </figure>
    </a>
    <a href="/project?p=qplum">
        <figure>
            <img src="qplum.jpg" alt="Qplum Logo">
            <div class="bg-only"></div>
            <figcaption>Qplum</figcaption>
        </figure>
    </a>
    <a href="/project?p=zoomcar">
        <figure>
            <img src="zoomcar.png" alt="Zoomcar Logo">
            <div class="bg-only"></div>
            <figcaption>Zoomcar</figcaption>
        </figure>
    </a>
    <a href="/project?p=lenskart">
        <figure>
            <img src="lenskart.svg" alt="Lenskart Logo">
            <div class="bg-only"></div>
            <figcaption>Lenskart Design</figcaption>
        </figure>
    </a>
    <a href="/project?p=idea">
        <figure>
            <img src="idea.svg" alt="Idea Design Workshop">
            <div class="bg-only"></div>
            <figcaption>Idea Design Workshop</figcaption>
        </figure>
    </a>
    <a href="/project?p=logo">
        <figure>
            <img src="logo.svg" alt="Logo Design">
            <div class="bg-only"></div>
            <figcaption>Logo Design</figcaption>
        </figure>
    </a>
</section>
<style>
    section {
        margin: 4rem 0;
        display: grid;
        justify-content: center;
        grid-gap: 0.75rem;
        grid-template-columns: repeat(3, 20rem);
        grid-auto-rows: calc(20rem / 1.69);
    }

    @media (max-width: 900px) {
        section {
            grid-template-columns: repeat(auto-fill, 20rem);
        }
    }

    .bg-only {
        visibility: hidden;
        position: absolute;
        background: #000;
        color: #FFF;
        opacity: 0;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: opacity 300ms cubic-bezier(.33,0,.2,1);
    }

    figcaption {
        visibility: hidden;
        position: absolute;
        background: transparent;
        color: #FFF;
        font-size: 1.5em;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    a,
    a:active,
    a:hover,
    a:focus {
        position: relative;
        text-decoration: none;
    }

    a {
        background-color: #d8d8d8;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    a:hover .bg-only {
        visibility: visible;
        opacity: 0.75;
    }

    a:hover figcaption {
        visibility: visible;
    }

    figure {
        margin: 0;
        margin-block: 0;
    }

    a:first-child {
        background-color: #7ab83166;
    }

    a:nth-child(2) {
        background-color: #f7b50040;
    }

    a:nth-child(3) {
        background-color: #e0f0ce;
    }

    a:nth-child(4) {
        background-color: #3b9f954d;
    }

    a:nth-child(5) {
        background-color: rgba(31, 61, 145, 0.2);
    }

    a:nth-child(5) > figure {
        width: 85px;
        height: 85px;
    }

    a:nth-child(6) {
        background-color: #b620e02e;
    }
</style>
