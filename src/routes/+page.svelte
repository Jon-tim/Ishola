<script>
	import Connect from '$lib/components/UI/Connect.svelte';
	import Introduction from '$lib/components/UI/Introduction.svelte';
	import Now from '$lib/components/UI/Now.svelte';
	import Projects from '$lib/components/UI/Projects.svelte';
	import Footer from '$lib/components/UI/Footer.svelte';
</script>

<svelte:head>
	<title>Oluwatimilehin Awoniyi</title>
	<meta name="description" content="Oluwatimilehin Awoniyi" />
</svelte:head>
<main>
	<section>
		<div class="container">
			<Introduction />
			<Projects />
			<Now />
			<Connect />
		</div>
	</section>
	<Footer />
</main>

<style>
	main {
		width: 100%;
		background: var(--bg-colour);
	}

	section {
		grid-column: 2/3;
	}

	.container {
		width: 100%;
		position: relative;
		padding-bottom: 2rem;
	}

	/* @media screen and (min-width: 768px) {
		main {
			background: #000;
		}
	} */

	@media screen and (min-width: 1024px) {
		main {
			display: grid;
			grid-template-columns: 1fr 700px 1fr;
		}
	}
</style>
