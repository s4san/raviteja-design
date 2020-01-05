<section>
    <a href="#">
        <img src="lmd-logo.svg" alt="LMD Logo">
    </a>
    <a href="#">
        <img src="qplum.jpg" alt="Qplum Logo">
    </a>
    <a href="#">
        <img src="zoomcar.jpg" alt="Zoomcar Logo">
    </a>
    <a href="#"></a>
    <a href="#"></a>
    <a href="#"></a>
    <a href="#"></a>
    <a href="#"></a>
    <a href="#"></a>
</section>
<style>
    section {
        margin: 4rem 0;
        display: grid;
        grid-gap: 12px;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: repeat(3, calc((70vw - 24px) / 3 / 1.69));
    }

    a {
        background-color: #d8d8d8;
        display: flex;
        align-items: center;
        justify-content: center;
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
</style>
