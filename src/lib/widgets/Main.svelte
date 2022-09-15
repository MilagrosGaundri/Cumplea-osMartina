<script lang="ts">
	import { fade, blur, fly, slide, scale } from 'svelte/transition';
	import { quintOut } from 'svelte/easing';
	import BoopAction from '../components/BoopAction.svelte';
	import Countdown from '$lib/components/Countdown.svelte';
	import Icon from '$lib/components/Icon.svelte';

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
				Te invita a su fiesta de Cumpleaños <!-- en... -->
				<!-- <br />
				Destellos Eventos -->
			</p>
		</div>
		<div>
			<div class="iconoDate">
				<Icon value='date-time'/>
			</div>
			<div class="cuandoDato">
				<h1>¿Cuando?</h1>
				<h3>
					Domingo 23 de octubre de 2022
					<br />
					17:00 hs
				</h3>
			</div>
		</div>

		<div class="Countdown">
			<Countdown/>
		</div>
	</div>
	<div class="ubicacion">
		<div class="texto">
		<h1>¿En dónde?</h1>
		<h3>
			Salón de eventos: Destellos Eventos
			<br />
			Canadá 3319, Lanús Oeste
		</h3>
		</div>
		<div class="ubi">
			<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3280.146761638954!2d-58.42071682122356!3d-34.70147808053005!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x95bccc56158a526f%3A0x867392d0bcc31e5d!2sDestellos%20Eventos!5e0!3m2!1ses-419!2sar!4v1663211850609!5m2!1ses-419!2sar" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
		</div>
	</div>
</div>



<style>
	*{
		width:425px;
		max-width: 425px;
		margin: 0;
		padding: 0;
		color: var(--cuatry-background);
	}
	.Main{ 
		background-color: var(--secondary-background);
		background-image: url('/images/background4.png'); 
		background-repeat: no-repeat;
		background-size: 100%;
		position: static;
	}
	.Main .headerM{
		/* animation: imgM 3s; */
		font-size: 12px;
		margin-top: 50px;
	}
	.Main .headerM .prestDisney {
		/* animation: imgM 3s; */
		font-size: 12px;
	}
	.Main .bodyM {
		/* animation: nameM 8s; */
		margin-top: 550px;
	}
	.Main .bodyM h1, h2 {
		font-size: 50px;
		margin: 0px;
		color: var(--secondary-background);
		text-shadow: 0.1em 0.1em 0.2em var(--cuartry-background);
	}
	.Main .bodyM h2 {
		font-size: 20px;
		margin: 0px;
	}
	/* .Main .text{
        animation: fade 8s;
      } */
  	.Main .text p {
		color: var(--cuartry-background);
		text-shadow: 0.1em 0.1em 0.2em var(--primary-background);
		font-size: 27px;
	}
	.Main .text .iconoDate{
		font-size: 45px;
		margin-top: 20px;
	}
	.Main .text .cuandoDato h3, h1{
		color: var(--cuartry-background);
		text-shadow: 0.1em 0.1em 0.2em var(--primary-background);
		margin: 0px;
	}
	.Main .separador{
       margin-bottom: 70px;
    }
	.Main .separador .img{
	   /* animation: fade 3s; */
		text-align: center;
	   	align-items: center;
		   position: absolute;
		z-index: 1;
	}
	.Main .separador .img img{
		text-align: center;
		align-items: center;
		margin-top: 10px;
		left: 160px;
		width: 150px;
		position: absolute;
		z-index: 1;
	}
	.Main .separador .waves {
		position: relative;
		width:460px;
		height: 70px;
	}
	.Main .ubicacion {
		padding: 30px 0px;
		margin: 40px 0px;
		background-color: var(--primary-background);
	}
	.Main .ubicacion .texto h1,h3{
		padding-bottom: 30px;
		color: var(--secondary-background);
		text-shadow: 0.1em 0.1em 0.2em var(--cuatry-background);
		margin: 0px;
	}
	.Main .ubicacion .ubi iframe{
		width: 80%;
		height: 200px;
		border-radius: 5%;
		border: 1px solid black;
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
