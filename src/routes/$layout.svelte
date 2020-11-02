<Nav />

<main class="content">
    <slot></slot>
</main>

<script>
    import Nav from '$components/Nav.svelte';
</script>

<style global>
html {
	padding: 0;
	margin: 0;
	background: #333;
}

body {
	padding: 0;
	margin: 0;
	display: flex;
	flex-wrap: wrap;
}

.content {
	/* text-align: center; */
	padding: 1rem 3rem;
	margin: 1rem 3rem;
	background-color: #dadada;
	flex-grow: 1;
}
</style>