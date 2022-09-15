<script lang="ts">
	import { onMount } from 'svelte';
	import Main from '$lib/widgets/Main.svelte';
</script>

<svelte:head>
	<title>Cumpleaños de Martina</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="contenedor">
	<Main />
</div>
<style>
	*{
		margin: auto 0;
		padding: 0;
	}
	.contenedor{
		display:flex;
    	justify-content:center;
		margin-top: -20px;
	}
	@font-face {
		font-family: Moanas;
		src: url('/fonts/Moanas.ttf');
	}
		:global(body) {
			/* background-color: var(--primary-background);
			background-image: url('/images/background4.png'); 
			background-repeat: no-repeat;
			background-size: 100%; */
			font-family: Moanas;
			color: var(--secondary-background);
			font-family: Moanas;
			text-align: center;
			text-shadow: 0.1em 0.1em 0.2em black;
		}
		:root {
			--primary-background: #c59b79;
			--secondary-background: #ffffff;
			--tertiary-background: #40b4fb;
		}
</style>
