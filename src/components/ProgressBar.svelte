<script>
   export let progress;
</script>
<style>
    .progress-bar {
        border : 1px solid rgb(163, 162, 162);
        margin: 10px 0px;
    }
    .progress {
        background-color: rgb(62, 214, 133);
      padding:10px
    }
    
</style>



<div class = "progress-bar" >
    <div class="progress" id="pb" style ="width:{progress}%;"><span class="sr-only" >{progress}</span></div>
</div>
