<script lang="ts">
  export let dateCountdown: any = "Oct 23, 2022 17:00:00";

    const second = 1000,
      minute = second * 60,
      hour = minute * 60,
      day = hour * 24;

    let dias:any;
    let horas:any;
    let minutos:any;
    let segundos:any;

    let countDown: any  = new Date(dateCountdown).getTime(),
    x = setInterval(function() {

      let now: any  = new Date().getTime(),
          distance = countDown - now;

          dias= Math.floor(distance / (day));
          horas = Math.floor((distance % (day)) / (hour));
          minutos = Math.floor((distance % (hour)) / (minute));
          segundos = Math.floor((distance % (minute)) / second);
    }, second)
</script>

<div class="contenedor">
  <figure class="cartel">
      <div id="dias" >{dias}</div>
      <div class="h3"><h3>Días</h3></div>
      <svg class="progress-ring" height="120" width="120">
        <circle
          class="progress-ring__circle"
          stroke-width="5"
          fill="transparent"
          r="45"
          cx="60"
          cy="60"
        />
      </svg>
  </figure>
  <figure class="cartel">
      <div id="horas">{horas}</div>
      <div class="h3"><h3>Horas</h3></div>
      <svg class="progress-ring" height="120" width="120">
        <circle
          class="progress-ring__circle"
          stroke-width="5"
          fill="transparent"
          r="45"
          cx="60"
          cy="60"
        />
      </svg>
  </figure>
  <figure class="cartel">
      <div id="minutos">{minutos}</div>
      <div class="h3"><h3>Minutos</h3></div>
        <svg class="progress-ring" height="120" width="120">
          <circle
            class="progress-ring__circle"
            stroke-width="5"
            fill="transparent"
            r="45"
            cx="60"
            cy="60"
          />
        </svg>
  </figure>
  <figure class="cartel">
      <div id="segundos">{segundos}</div>
      <div class="h3"><h3>Segundos</h3></div>
          <svg class="progress-ring" height="120" width="120">
            <circle
              class="progress-ring__circle"
              stroke-width="5"
              fill="transparent"
              r="45"
              cx="60"
              cy="60"
            />
          </svg>
  </figure>
    
      <!-- <div class="cartel">
        <div id="dias" >{dias}</div>
        <div class="h3"><h3>Días</h3></div>
      </div>
      <div class="cartel">
        <div id="horas">{horas}</div>
        <div class="h3"><h3>Horas</h3></div>
      </div>
      <div class="cartel">
        <div id="minutos">{minutos}</div>
        <div class="h3"><h3>Minutos</h3></div>
      </div>
      <div class="cartel">
        <div id="segundos">{segundos}</div>
        <div class="h3"><h3>Segundos</h3></div>
      </div> -->
</div>


<style>
  .contenedor {
    padding: 20px 0px;
  }
  .contenedor .cartel {
    width: 20%;
    padding: 3px;
    display: inline-block;
    position: relative;
    justify-content: center;
    align-items: center;
    font-size: 20px;
    padding-top: 10px;
    margin: 0px 2px;
}
.progress-ring {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.progress-ring__circle {
  transition: 0.5s;
  transform: rotate(-90deg);
  transform-origin: 50% 50%;
  stroke: rgb(230, 230, 230);
}

  .contenedor{    
    color: var(--secondary-background); 
        width: 100%;
        text-align: center;
        align-items: center;
  }
  .cartel > div {
    /* font-size: 15px; */
    animation: fade 3s;
    margin-top: 5px;
  }
  .cartel > div > h3 {
    margin-top: 5px;
    font-size: 13px;
    font-weight: normal;
  }
  .h3 {
    bottom: 0;
    margin: 0 auto;
  }
  .contenedor {
    margin-top: 3%;
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
</style>
