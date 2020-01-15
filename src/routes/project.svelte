<script>
    import { onMount, setContext } from 'svelte';
    import Project from '../components/Project.svelte';

    const PROJECT_DATA = {
        zoomcar: {
            title: 'Zoomcar App',
            url: '/zoomcar.pdf'
        },
        lmd: {
            title: 'LMD (Last Mile Delivery)',
            url: '/LMD.pdf'
        },
        qplum: {
            title: 'qplum - Account Opening Design',
            url: '/qplum.pdf'
        },
        lenskart: {
            title: 'Lenskart',
            url: '/lenskart.pdf'
        },
        idea: {
            title: 'The Idea Centre',
            url: '/idea.pdf'
        },
        logo: {
            title: 'Logo Design',
            url: '/logo.pdf'
        },
        resume: {
            title: 'Resume',
            url: '/resume.pdf'
        }
    };
    try {
        if (location) {
            const query = new URLSearchParams(location.search);
            const key = query.get('p') || 'zoomcar';
            const { title, url } = PROJECT_DATA[key];
            setContext('project', {
                title,
                url
            });
        }
    } catch (e) {
        setContext('project', {
            title: '',
            url: ''
        });
    }
</script>
<Project loaded={false}/>
<div id="loader" style="position: relative; min-height: 400px;">
    <div class="loading"></div>
</div>
