<script lang="ts">
	import { onMount } from 'svelte';
	import Main from '$lib/widgets/Main.svelte';
</script>

<svelte:head>
	<title>Cumpleaños de Martina</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Main />
</section>
<style>

	@font-face {
		font-family: Moanas;
		src: url('/fonts/Moanas.ttf');
	}
		:global(body) {
			margin: 0;
			padding: 0;
			width: 100%;
			/* background-image: url('/images/background4.png'); 
			background-repeat: no-repeat;
			background-size: 100%; */
			color: var(--tertiary--background);
			font-family: Moanas;
			max-width: 430px;
		}
		:global(h1, h2, h3, p) {
			color: var(--secondary-background);
			font-family: Moanas;
			font-weight: normal;
			font-style: normal;
			text-align: center;
		}
		:root {
			--primary-background: #c59b79;
			--secondary-background: #ffffff;
			--tertiary-background: #40b4fb;
		}
	section{
		align-items: center;
		text-align: center;
	}
</style>
