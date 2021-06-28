<script>
    import { tripCount } from "../store/store.js";
</script>

<div class="Navbar">
    <h1>Available Schedules</h1>
    <h4>Selections: {$tripCount}</h4>
</div>


<style>
    h1 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 3em;
        font-weight: 100;
    }

    .Navbar{
        display: flex;
        justify-content: space-between;
    }
</style>
