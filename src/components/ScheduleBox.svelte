<script>
    import { tripCount } from "../store/store";
    export let schedule;
    let selected = false;

    function handleClick() {
        if ($tripCount >= 8 && !selected) return;
        selected = !selected;
        if (selected) {
            tripCount.update((n) => (n = n + 1));
        } else {
            tripCount.update((n) => (n = n - 1));
        }
    }
</script>

<div class="ScheduleBox">
    <div class="ScheduleBox-content">
        <button
            type="button"
            on:click={handleClick}
            class:active-select={selected}
        >
            <h3>{schedule}</h3>
        </button>
    </div>
</div>

<style>
    .ScheduleBox {
        max-width: 10em;
        align-items: center;
    }

    .ScheduleBox-content {
        border-color: black;
    }

    .ScheduleBox-content button {
        min-width: 10em;
        border-radius: 40px;
    }

    .active-select {
        color: #18bc78;
        animation: bounce linear 0.8s;
        animation-iteration-count: 1;
        transform-origin: 20% 20%;
    }
</style>
