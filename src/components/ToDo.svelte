<script>
    let itemstodo = [
        { done: false, text: "laundry" },
        { done: false, text: "fix bike" },
        { done: false, text: "troll more" },
    ];

    function add() {
        itemstodo = itemstodo.concat({ done: false, text: "" });
    }

    function clear() {
        itemstodo = itemstodo.filter((t) => t.done).length;
    }

    $: remaining = itemstodo.filter((t) => !t.done).length;
</script>

{#each itemstodo as itemtodo}
    <div class:done={itemtodo.done}>
        <input type="checkbox" bind:checked={itemtodo.done} />

        <input placeholder="add something here" bind:value={itemtodo.text} />
    </div>
{/each}

<p>{remaining} remaining</p>

<button on:click={add}> Add new </button>

<button on:click={clear}> Clear completed </button>

<style>
    .done {
        opacity: 0.4;
    }
</style>
