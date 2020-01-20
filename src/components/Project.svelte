<script>
    import { onMount } from 'svelte';
    import { getContext } from 'svelte';
    import pdfjs from "@bundled-es-modules/pdfjs-dist/build/pdf";
    import viewer from "@bundled-es-modules/pdfjs-dist/web/pdf_viewer";

    pdfjs.GlobalWorkerOptions.workerSrc = "https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.2.228/pdf.worker.min.js";
    let { title, url } = getContext('project');
    function removeLoader() {
        const divs = document.querySelectorAll('#loader');
        divs.forEach(div => {
            if (div) {
                div.style.display = 'none';
            }
        });
    }
    async function init() {
        const root = document.getElementById('pdf');
        const container = root.appendChild(document.createElement('div'));
        container.appendChild(document.createElement('div'));
        const pdfViewer = new viewer.PDFViewer({
            container: container,
            renderer: 'svg',
            textLayerMode: 0
        });
        document.addEventListener("pagesinit", function() {
            // We can use pdfViewer now, e.g. let's change default scale.
            pdfViewer.currentScaleValue = "page-width";
        });
        const loadingTask = pdfjs.getDocument(url);
        const pdf = await loadingTask.promise;
        pdfViewer.setDocument(pdf);
        removeLoader();
    }

    onMount(init);
</script>
<style>
    div {
        height: auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    h1 {
        text-align: center;
    }
</style>
<div id="pdf">
    <h1>{title}</h1>
</div>
