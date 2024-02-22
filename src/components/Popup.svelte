<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  export let onClose;
</script>

<h2>This is a popup</h2>
<button on:click={onClose}>Close popup via props</button>
<button
  on:click={() =>
    dispatch("close", {
      message: "Popup is closed via Event Dispatcher",
    })}>Close popup via Event Dispatcher</button
>
