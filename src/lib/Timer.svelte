<script>
    import Progressbar from "./Progressbar.svelte";
    const totalSecondsLeft = 20;
    let secondsLeft = totalSecondsLeft;
    var remaining = 0;
    $: progress = ((totalSecondsLeft - secondsLeft) / totalSecondsLeft) * 100;

    function startTimer(){
        let timer = setInterval(reduceSeconds, 1000)

        function reduceSeconds(){
            secondsLeft -= 1
            if (secondsLeft <= 0){
                clearInterval(timer);
            }
            remaining += 1; 
        }
    }

    function resetTimer(){
        secondsLeft = 20;
    }

</script>

<h2 class="mr7 tc">Seconds Left:{secondsLeft}</h2>
<h2 class="mr7 tc">Seconds Completed:{remaining}</h2>

<Progressbar {progress}/>

<div class="ph3 justify-center flex">
    <button class="f3 br1 ph3 ml2 pv2 mb2 white bg-black" on:click={startTimer}>Start Timer</button>
    <button class="f3 br1 ph3 ml2 pv2 mb2 white bg-blue" on:click={resetTimer}>Reset Timer</button>
</div>
