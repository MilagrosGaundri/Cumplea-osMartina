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
			background-color: #161616;
			/* background-image: url('/images/background4.png'); 
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
			--cuatry-background: #000000;
			--quinty-background: #2e2e2e;
			--sexty-background: #e0e0e0;
			--mar-background: #6EC9DA;
			--mar1-background: #003b46;
			--mar2-background: #07575b;
			--mar3-background: #86cbd4;
			--mar4-background: #C4DFE6;
			--marpruebamar-background: #d1f5fc;
		}
</style>
