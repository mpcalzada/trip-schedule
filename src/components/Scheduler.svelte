<script>
    import ScheduleBox from "./ScheduleBox.svelte";

    const availableSchedules = generateSchedules();

    function generateSchedules() {
        const schedules = [];
        let date = new Date();
        date.setHours(8);
        date.setMinutes(0);
        do {
            let formatTime = formatSchedule(date.getHours()) + ":" + formatSchedule(date.getMinutes())
            date.setTime(date.getTime() + 30 * 60 * 1000);
            schedules.push(formatTime);
        } while (date.getHours() != 20 || date.getMinutes() != 30);
        return schedules;
    }

    function formatSchedule(time) {
        if (time.toString().length > 1) {
            return time;
        }
        return "0" + time;
    }
</script>

<div class="Scheduler">
    <div class="Scheduler-title" />
    <div class="Scheduler-content">
        {#each availableSchedules as schedule}
            <ScheduleBox {schedule} />
        {/each}
    </div>
</div>

<style>
    .Scheduler-content {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        max-width: 70em;
    }
</style>
