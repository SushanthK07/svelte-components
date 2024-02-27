<script>
  import TabA from "./TabA.svelte";
  import TabB from "./TabB.svelte";
  import TabC from "./TabC.svelte";

  let activeTab = TabA;

  function handleTabChange(tab) {
    activeTab = tab;
  }
</script>

<main>
  <h2>Dynamic Component</h2>
  <div>
    <button
      class={activeTab === TabA ? "border" : ""}
      on:click={() => handleTabChange(TabA)}
    >
      Tab A
    </button>
    <button
      class={activeTab === TabB ? "border" : ""}
      on:click={() => handleTabChange(TabB)}
    >
      Tab B
    </button>
    <button
      class={activeTab === TabC ? "border" : ""}
      on:click={() => handleTabChange(TabC)}
    >
      Tab C
    </button>
  </div>

  <!-- {#if activeTab === "A"}
    <TabA />
  {:else if activeTab === "B"}
    <TabB />
  {:else if activeTab === "C"}
    <TabC />
  {/if} -->

  <!--
    svelte specific html tag 'svelte:component'
    role: renders the svelte component dynamically by setting this attribute
  -->
  <svelte:component this={activeTab} />
</main>

<style>
  .border {
    border: 1px solid purple;
  }
</style>
