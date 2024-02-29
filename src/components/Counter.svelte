<script context="module">
  let totalCount = 0;

  export function getTotalCount() {
    return totalCount;
  }
</script>

<script>
  let count = 0;

  function handleIncrement() {
    count += 1;
    totalCount += 1;
  }
</script>

<main>
  <h3>Count: {count}</h3>
  <button on:click={handleIncrement}>Increase</button>
</main>
