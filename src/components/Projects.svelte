<section>
    <a href="/project?p=lmd">
        <figure>
            <img src="lmd-logo.svg" alt="LMD Logo">
            <figcaption>Last Mile Delivery</figcaption>
        </figure>
    </a>
    <a href="/project?p=qplum">
        <figure>
            <img src="qplum.jpg" alt="Qplum Logo">
            <figcaption>Qplum</figcaption>
        </figure>
    </a>
    <a href="/project?p=zoomcar">
        <figure>
            <img src="zoomcar.png" alt="Zoomcar Logo">
            <figcaption>Zoomcar</figcaption>
        </figure>
    </a>
    <a href="/project?p=lenskart">
        <figure>
            <img src="lenskart.svg" alt="Lenskart Logo">
            <figcaption>Lenskart Design</figcaption>
        </figure>
    </a>
    <a href="/project?p=idea">
        <figure>
            <img src="idea.svg" alt="Idea Design Workshop">
            <figcaption>Idea Design Workshop</figcaption>
        </figure>
    </a>
    <a href="/project?p=logo">
        <figure>
            <img src="logo.svg" alt="Logo Design">
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

    figcaption {
        visibility: hidden;
        height: 0;
    }

    a,
    a:active,
    a:hover,
    a:focus {
        text-decoration: none;
    }

    a {
        background-color: #d8d8d8;
        display: flex;
        align-items: center;
        justify-content: center;
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
