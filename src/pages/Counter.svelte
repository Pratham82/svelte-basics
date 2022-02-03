<script>
  import Header from '../components/Header.svelte'
  let count = 0
  const operations = ['Increment +', 'Reset', 'Decrement -']
  const handleOperation = operation => {
    operation === 'Increment +'
      ? count++
      : operation === 'Decrement -'
      ? count > 0 && count--
      : (count = 0)
  }
</script>

<Header headerTitle="Counter" />
<h2>{count}</h2>
{#each operations as operation}
  <button
    class={operation === 'Increment +'
      ? 'btn inc'
      : operation === 'Decrement -'
      ? 'btn dec'
      : 'btn'}
    on:click={() => handleOperation(operation)}>{operation}</button
  >
{/each}

<style>
  /* your styles go here */
  .btn {
    margin: 0 5px;
    border: none;
    border-radius: 5px;
    padding: 10px 15px;
    background-color: antiquewhite;
    cursor: pointer;
  }
  .inc {
    color: green;
    background-color: lightgreen;
  }
  .dec {
    color: red;
    background-color: lightsalmon;
  }
  .btn:active,
  .inc:active,
  .dec:active {
    transform: scale(0.95);
    transition: 0.1s ease-in-out;
  }
</style>
