<script>
    import {tripCount} from '../store/store'
    export let schedule;

    function handleClick(){
        tripCount.update((n)=>n = n+1)
    }
</script>

<div class="ScheduleBox">
    <div class="ScheduleBox-content">
        <h3>{schedule}</h3>
    </div>
    <div class="ScheduleBox-button">
        <button type="button" on:click={handleClick}>Select</button>
    </div>
</div>

<style>
    .ScheduleBox{
        max-width: 10em;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    .ScheduleBox-content {
        border-color: black;
    }
</style>