<script>
    import Text from "./Text.svelte";
    import ToDo from "./ToDo.svelte";
    export let name = "YOUR_NAME";
    new todo = new ToDo({
        // some code here
})
</script>

<main>
    <input bind:value={name} />

    <h1>This is <name>'s To Do List!</name></h1>
    <Text />
</main>

<style>
</style>
