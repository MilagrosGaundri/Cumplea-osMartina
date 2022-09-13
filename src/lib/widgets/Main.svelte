<script  lang="ts">
    import { fade, blur, fly, slide, scale } from "svelte/transition";
    import { quintOut } from "svelte/easing";
    import BoopAction from '../components/BoopAction.svelte';
    import Countdown from "$lib/components/Countdown.svelte";
    //   import Icons from '../components/Icons.svelte';
  </script>
  
  <div class="Main">
    <div class="headerM">
        <p class="prestDisney">Disney presenta</p>
    </div>
    <div class="bodyM">
        <BoopAction boopParams={{ scale: 1.2, timing: 200}}>
            <h1>MARTINA</h1> 
        </BoopAction>
        <h2>Mis 7 años</h2>
    </div> 
    <div class="separador">
    </div>
    <div class="text">
      <div>
        <p>Te invita a su fiesta
          de Cumpleaños
          en... 
          <br>
            Destellos Eventos
        </p> 
      </div>
      <div>
        <p>¿Cuando?</p>
        Domingo 23 de octubre de 2022
        <br>
        17:00 hs
      </div>
      
      <div class="Countdown">
        <Countdown/>
      </div>
        
    </div>
  </div>
  <style>
    :global(button:focus) {
		outline: 3px solid black;
	}
      .Main {
        justify-content: center;
        align-items: center;
        text-align: center;
        
      } 
      .Main .headerM {
        width: 100%;
        z-index: 1;
      }
      .Main .headerM .prestDisney{
        font-size: 12px;
        z-index: 1;
      }
      .Main .bodyM{
        margin-top: 500px;
        margin-bottom: 50px;
      }
      .Main .bodyM h1{
        font-size: 50px;
        margin: 0px;
      }
      .Main .bodyM h2{
        font-size: 20px;
        margin: 0px;
      }
    
      /* .disney{
        text-align:center;
        position: absolute;
        top: 0;
        animation: imgM 3s;
        z-index: -1; 
        width:100px;
        margin-top: 45px;
      } */
      /* .disney img{
       
      } */
  /* 
      .prueba{
        animation: fade 8s;
      }  */
      /* .Countdown{
        text-align: center;
        align-items: center;
      } */
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
  