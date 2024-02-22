<script>
  import { setContext } from "svelte";
  import Greet from "./components/Greet.svelte";
  import Popup from "./components/Popup.svelte";

  const name = "Modi";
  const superHeroName = "Prime Minister of India";

  const person = {
    name: "Virat Kohli",
    superHeroName: "GOAT",
  };

  setContext("user-info", { name: "Anonymous" });

  let showPopup = false;
  function handlePopupOpen() {
    showPopup = true;
  }

  function handlePopupClose(event) {
    if (event.detail) {
      console.log(event.detail);
    }
    showPopup = false;
  }
</script>

<main>
  <Greet superHeroName="HanuMan" />
  <Greet name="Phaneendra" superHeroName="IronMan" />
  <Greet name="Krishna" />
  <Greet {name} {superHeroName} />
  <Greet {...person} />
  <button on:click={handlePopupOpen}>Open Popup</button>
  {#if showPopup}
    <Popup onClose={handlePopupClose} on:close={handlePopupClose} />
  {/if}
</main>

<style>
</style>
