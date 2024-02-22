<script>
  import { createEventDispatcher } from "svelte";
  import Button from "./Button.svelte";

  const dispatch = createEventDispatcher();

  const greet = () => {
    dispatch("greet", "Hello from Inner");
  };
</script>

<button on:click={greet}>Greet</button>
