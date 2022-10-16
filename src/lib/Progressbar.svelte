<script>
    export let progress = 0;
</script>

<style>
    .bars{
        fill: green;
    }
</style>
<div class="flex justify-center">
    <svg width="100%" height="100">
        <g class='bars'>
                <rect
                    x= 310
                    y= 0
                    width={progress * 6.2}
                    height=30
                ></rect>
        </g>
    </svg>    
</div>
