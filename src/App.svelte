<script>
  import Timer from './lib/Timer.svelte'
  import Howto from './lib/Howto.svelte' 
  let myName;


</script>

<main>
  
  <div class="w-100 tc">
    <h1>
      Handwashing App
    </h1>    
  </div>
  <Timer/>
  <Howto/>
  <div class="flex justify-center">
    <h3><a href="https://www.who.int/teams/integrated-health-services/infection-prevention-control" class="pa1">Picture Source</a></h3>
    <h3><a href="https://www.who.int/teams/integrated-health-services/infection-prevention-control" class="pa1">Sound Source</a></h3>
  </div>
</main>

<style>
</style>
