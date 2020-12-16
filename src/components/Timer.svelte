<script>
    import ProgressBar from './ProgressBar.svelte';
    let totalSeconds=20;
    let seconds=0;
    let secondsLeft = totalSeconds;
    // let mytime = setInterval(calculateTime, 1000);
 
        function time(){
            
            let timer =  setInterval(()=>{
            document.getElementById('btn').disabled = true;
            seconds = seconds + 1;
            secondsLeft = totalSeconds - seconds;
            
            if(seconds ===20){
                clearInterval(timer);
                seconds = 0;
                document.getElementById('btn').disabled = false;
            }
        }, 1000);
           
        }

    
</script>
<style>
    button {
        width: 100%;
        background-color:rgb(236, 10, 115);
        color :white;
        margin: 10px 0;
    }
</style>
<p>Timer</p>
<h1>Seconds Left: {secondsLeft}</h1>
<ProgressBar progress ={seconds * 5}></ProgressBar>
<button id="btn" on:click="{time}">Start</button>