<script>
    import ScheduleBox from "./ScheduleBox.svelte";

    const availableSchedules = [];
    let date = new Date();
    date.setHours(8);
    date.setMinutes(0);
    do {
        let formatTime = date.getHours() + ":" + date.getMinutes();
        date.setTime(date.getTime() + 30 * 60 * 1000);
        availableSchedules.push(formatTime);
        console.log(availableSchedules);
    } while (date.getHours() != 20 || date.getMinutes() != 30);
    console.log(date.getHours() != 19 || date.getMinutes() != 30)

</script>

<div class="Scheduler">
    <div class="Scheduler-title" />
    <div class="Scheduler-content">
        {#each availableSchedules as schedule}
            <ScheduleBox {schedule} />
        {/each}
    </div>
</div>
