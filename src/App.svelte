<script>
  import Timer from './lib/Timer.svelte'
  import Howto from './lib/Howto.svelte' 
  let myName;
  let audio;

  function timerEnds(e){
    console.log(e)
    audio.play()
  }

</script>

<main>
  
  <div class="w-100 tc">
    <h1>
      Handwashing App
    </h1>    
  </div>
  <Timer on:end={timerEnds}/>
  <Howto/>
  <div class="flex justify-center">
    <h3><a href="https://www.who.int/teams/integrated-health-services/infection-prevention-control" class="pa1">Picture Source</a></h3>
    <h3><a href="https://www.who.int/teams/integrated-health-services/infection-prevention-control" class="pa1">Sound Source</a></h3>
  </div>

  <audio bind:this={audio}>
    <source src="./src/assets/public_sound.wav">
  </audio>
</main>
