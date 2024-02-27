<script>
  import { onMount } from "svelte";

  let inputRef;

  onMount(() => {
    if (inputRef) {
      inputRef.focus();
    }
  });
</script>

<main>
  <label for="name">Name</label>
  <input type="text" name="name" id="name" bind:this={inputRef} />
</main>
