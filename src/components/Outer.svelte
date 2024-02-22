<script>
  import Inner from "./Inner.svelte";

  const greetHandler = (event) => {
    console.log(event.detail);
  };
</script>

<!-- events the listened by the immediate parent when it is emitted by their children -->
<!-- <Inner on:greet={greetHandler} /> -->

<!-- to forward the events, to the next parent, simply omit handling the event, svelte considers it as forwarding the event to next immediate parent -->
<Inner on:greet />
