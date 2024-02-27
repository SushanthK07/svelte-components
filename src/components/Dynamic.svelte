<script>
  import TabA from "./TabA.svelte";
  import TabB from "./TabB.svelte";
  import TabC from "./TabC.svelte";

  let mainTab = "A";

  function handleTabChange(tab) {
    mainTab = tab;
  }
</script>

<main>
  <h2>Dynamic Component</h2>
  <div>
    <button
      class={mainTab === "A" ? "border" : ""}
      on:click={() => handleTabChange("A")}
    >
      Tab A
    </button>
    <button
      class={mainTab === "B" ? "border" : ""}
      on:click={() => handleTabChange("B")}
    >
      Tab B
    </button>
    <button
      class={mainTab === "C" ? "border" : ""}
      on:click={() => handleTabChange("C")}
    >
      Tab C
    </button>
  </div>
  {#if mainTab === "A"}
    <TabA />
  {:else if mainTab === "B"}
    <TabB />
  {:else if mainTab === "C"}
    <TabC />
  {/if}
</main>

<style>
  .border {
    border: 1px solid purple;
  }
</style>
