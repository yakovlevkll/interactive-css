<header class="site-header">
    <nav>
        <a href="/" class="site-logo">Interactive CSS</a>
    </nav>
</header>

<nav class="site-sidebar">
    {#each routes as route (route.link)}
    <a href={route.link}>{route.text}</a>
    {/each}
</nav>

<script>
    const routes = [
        {
            text: 'Background',
            link: '/background'
        },
        {
            text: 'Border',
            link: '/border'
        },
        {
            text: 'Color',
            link: '/color'
        },
        {
            text: 'Image',
            link: '/image'
        },
        {
            text: 'Margin',
            link: '/margin'
        },
        {
            text: 'Media query',
            link: '/media-query'
        },
        {
            text: 'Padding',
            link: '/padding'
        },
        {
            text: 'Position',
            link: '/position'
        },
        {
            text: 'Selectors',
            link: '/selectors'
        },
        {
            text: 'Shadow',
            link: '/shadow'
        },
        {
            text: 'Text',
            link: '/text'
        },
        {
            text: 'Variables',
            link: '/variables'
        },
    ]
</script>

<style global>
.site-header {
    flex-basis: 100%;
}

.site-header nav {
    height: 10vh;
    padding: 0.25rem 1.6rem;
    background: #232323;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);

    display: flex;
    align-items: center;
    gap: 1rem;
}

.site-header a {
    color: #eaeaea;
    text-decoration: none;
}

.site-logo {
    font-size: 1.5rem;
}

.site-sidebar {
    display: flex;
    flex-direction: column;
    padding: 1rem 2rem 1rem 1rem;
    gap: 0.5em;

    background-color: #2a2a2a;
}

.site-sidebar a {
    color: #dadada;
    text-decoration: none;
}
</style>