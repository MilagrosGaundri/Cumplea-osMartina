<script  lang="ts">
    // import Countdown from "../components/Countdown.svelte";
    //   import Icons from '../components/Icons.svelte';
  </script>
  
  <div class="Main">
    <div class="headerM">
        <p class="prestDisney">Disney presenta</p>
    </div>
    <div class="bodyM">
        <h3>MARTINA</h3> 
        <h3>Mis 7 años</h3>
    </div> 
    <div class="prueba">
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
      
      <!-- <div class="Countdown">
        <Countdown/>
      </div> -->
        
    </div>
  </div>
  <style>
      .Main {
        justify-content: center;
        align-items: center;
        text-align: center;
        
      } 
      .Main .headerM {
        width: 20px;
        z-index: 1;
      }.Main .headerM .prestDisney{
        width: 20px;
        z-index: 1;
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
  