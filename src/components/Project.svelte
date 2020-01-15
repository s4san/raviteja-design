<script>
    import { onMount } from 'svelte';
    import { getContext } from 'svelte';
    let { title, url } = getContext('project');
    let loaded = false;

    export async function setupPdfJS() {
        function removeLoader() {
            const divs = document.querySelectorAll('#loader');
            divs.forEach(div => {
                if (div) {
                    div.style.display = 'none';
                }
            });
        }
        try {
            if (typeof window !== 'undefined') {
                const root = document.getElementById('pdf');
                pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.3.200/pdf.worker.min.js';
                const loadingTask = pdfjsLib.getDocument(url);
                const pdf = await loadingTask.promise;
                const pages = pdf.numPages;
                loaded = true;
                for (let i = 1; i <= pages; ++i) {
                    const page = await pdf.getPage(i);
                    const scale = window.devicePixelRatio || 1.5;
                    const viewport = page.getViewport({ scale: scale });
                    //
                    // Prepare canvas using PDF page dimensions
                    //
                    const canvas = document.createElement('canvas');
                    root.append(canvas);
                    const context = canvas.getContext('2d');
                    canvas.height = viewport.height;
                    canvas.width = viewport.width;

                    //
                    // Render PDF page into canvas context
                    //
                    const renderContext = {
                        canvasContext: context,
                        viewport: viewport,
                    };
                    page.render(renderContext);
                }
                removeLoader();
            }
        } catch (e) {}
    }

    onMount(() => {
        if (!loaded) {
            setupPdfJS();
        }
    })
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
    <script id="pdfjs" src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.3.200/pdf.min.js" on:load={setupPdfJS}></script>
</div>
