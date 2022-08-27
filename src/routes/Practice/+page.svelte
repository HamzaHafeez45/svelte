<script>
  let x = 0;
  let y = 0;
  let name = "Hello World";
  let text =
    "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.";
  let list = [{ todo: "Task1" }, { todo: "Task2" }, { todo: "Task3" }];
</script>

<h1>Practice page</h1>
<h2>Counter</h2>

Total: {x}
<button on:click={() => x++}> Increment X </button>

<button class={x == 0 ? "disabled" : ""} on:click={() => x--}>
  decrement X
</button>
<br />
<input style:margin-top="2rem" bind:value={name} />
<textarea
  style:width="20rem"
  style:margin-top="2rem"
  style:height="10rem"
  bind:value={text}
/>

<button on:click={() => alert(name)}>Alert Name</button>

<h1>Here is the List of todos</h1>
<ul>
  {#each list as item}
    <li>{item.todo}</li>
  {/each}
</ul>

<style>
  :global(h1) {
    color: Red;
  }
  h1 {
    color: Green;
  }
  button {
    color: white;
    background: black;
  }
  .disabled {
    pointer-events: none;
    background: grey;
  }
</style>
