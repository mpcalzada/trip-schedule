<script>
    import { tripCount } from "../store/store.js";
</script>

<div class="Navbar">
    <h1>Available Schedules</h1>
    <h4>Selections: {$tripCount}</h4>
</div>


<style>
    h1 {
        color: #3476b5;
        text-transform: uppercase;
        font-size: 3em;
        font-weight: 100;
        font-family: serif;
        padding: 0 0 0 2em;
    }

    h4{
        color: #3476b58c;
        font-size: 2em;
        font-family: serif;
        padding: 0 2em;
    }

    .Navbar{
        display: flex;
        justify-content: space-between;
    }
</style>
