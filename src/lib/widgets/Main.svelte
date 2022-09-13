<script lang="ts">
	import { fade, blur, fly, slide, scale } from 'svelte/transition';
	import { quintOut } from 'svelte/easing';
	import BoopAction from '../components/BoopAction.svelte';
	import Countdown from '$lib/components/Countdown.svelte';
	//   import Icons from '../components/Icons.svelte';
</script>

<div class="Main">
	<div class="headerM">
		<p class="prestDisney">Disney presenta</p>
	</div>
	<div class="bodyM">
		<BoopAction boopParams={{ scale: 1.2, timing: 200 }}>
			<h1>MARTINA</h1>
		</BoopAction>
		<h2>Mis 7 años</h2>
	</div>
	<div class="separador">
		<div class='img'>
			<img src="/images/logo.png" alt="">
		</div>
		<svg
			class="waves"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
			viewBox="0 24 150 28"
			preserveAspectRatio="none"
			shape-rendering="auto"
		>
			<defs>
				<path
					id="gentle-wave"
					d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"
				/>
			</defs>
			<g class="parallax">
				<use xlink:href="#gentle-wave" x="48" y="0" fill="rgba(255,255,255,0.7" />
				<use xlink:href="#gentle-wave" x="48" y="3" fill="rgba(255,255,255,0.5)" />
				<use xlink:href="#gentle-wave" x="48" y="5" fill="rgba(255,255,255,0.3)" />
				<use xlink:href="#gentle-wave" x="48" y="7" fill="#fff" />
			</g>
		</svg>
	</div>
	<div class="text">
		<div>
			<p>
				Te invita a su fiesta de Cumpleaños en...
				<br />
				Destellos Eventos
			</p>
		</div>
		<div>
			<p>¿Cuando?</p>
			Domingo 23 de octubre de 2022
			<br />
			17:00 hs
		</div>

		<div class="Countdown">
        <Countdown/>
      </div>
	</div>
</div>



<style>
	.Main .headerM .prestDisney {
		animation: imgM 3s;
		font-size: 12px;
	}
	.Main .bodyM {
		animation: nameM 8s;
		margin-top: 580px;
	}
	.Main .bodyM h1 {
		font-size: 50px;
		margin: 0px;
	}
	.Main .bodyM h2 {
		font-size: 20px;
		margin: 0px;
	}
  .Main .text p {
    color: var(--primary-background);
	}
	.Main .separador{
       margin-bottom: 70px;
    }
	.Main .separador .img{
		text-align: center;
	   	align-items: center;
	}
	.Main .separador .img img{
		margin-top: 10px;
		left: 160px;
		width: 150px;
		position: absolute;
		z-index: 1;
	}
	.Main .separador .waves {
		position: relative;
		width:460px;
		left: -5%;
		height: 70px;
	}
	.Main .text{
        animation: fade 8s;
      }
	@keyframes fade {
		0% {
			opacity: 0;
		}
		30% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	.parallax > use {
		animation: move-forever 25s cubic-bezier(0.55, 0.5, 0.45, 0.5) infinite;
	}
	.parallax > use:nth-child(1) {
		animation-delay: -2s;
		animation-duration: 7s;
	}
	.parallax > use:nth-child(2) {
		animation-delay: -3s;
		animation-duration: 10s;
	}
	.parallax > use:nth-child(3) {
		animation-delay: -4s;
		animation-duration: 13s;
	}
	.parallax > use:nth-child(4) {
		animation-delay: -5s;
		animation-duration: 20s;
	}
	@keyframes move-forever {
		0% {
			transform: translate3d(-90px, 0, 0);
		}
		100% {
			transform: translate3d(85px, 0, 0);
		}
	}

	@keyframes nameM {
		0% {
			opacity: 0;
		}
		30% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	@keyframes imgM {
		0% {
			opacity: 0;
		}
		30% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	/* .Main-container {
        display: grid;
        grid-template-columns: 3fr 1fr;
        grid-gap: 2em;
        padding: 2em 0;
      } */
</style>
