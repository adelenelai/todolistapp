<script>
    import Text from "../components/Text.svelte";
    import ToDo from "../components/ToDo.svelte";
    export let name = "YOUR_NAME";
</script>

<h1>To Do List App</h1>
<p>Here's a simple app for making a To Do List!</p>

<main>
    <input bind:value={name} />

    <h1>This is {name}'s To Do List!</h1>
    <Text />
    <ToDo />
</main>

<style>
</style>
