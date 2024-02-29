<script>
  import { setContext } from "svelte";
  import Greet from "./components/Greet.svelte";
  import Popup from "./components/Popup.svelte";
  import Outer from "./components/Outer.svelte";
  import Card from "./components/Card.svelte";
  import Button from "./components/Button.svelte";
  import Names from "./components/Names.svelte";
  import ChildStyles from "./components/ChildStyles.svelte";
  import PostList from "./components/PostList.svelte";
  import AutoFocus from "./components/AutoFocus.svelte";
  import Dynamic from "./components/Dynamic.svelte";
  import Counter, { getTotalCount } from "./components/Counter.svelte";

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

  const greetHandler = (event) => {
    alert(event.detail);
  };
</script>

<main>
  <!-- <Greet superHeroName="HanuMan" />
  <Greet name="Phaneendra" superHeroName="IronMan" />
  <Greet name="Krishna" />
  <Greet {name} {superHeroName} />
  <Greet {...person} /> -->
  <!-- <button on:click={handlePopupOpen}>Open Popup</button>
  {#if showPopup}
    <Popup onClose={handlePopupClose} on:close={handlePopupClose} />
  {/if} -->
  <!-- <br /> -->
  <!-- <Outer on:greet={greetHandler} /> -->
  <!-- <Card />
  <Card>Card Content</Card>
  <Card>
    <h3>Card Content</h3>
  </Card>
  <Card>
    <img src="https://picsum.photos/300" alt />
  </Card> -->
  <!-- <Card>
    <div slot="header">
      <h2>Header</h2>
    </div>
    <div slot="content">
      <img src="https://picsum.photos/300" alt />
    </div>
    <div slot="footer">
      <Button>View More</Button>
    </div>
  </Card>
  <Card /> -->
  <!-- <Names>
    <h4 slot="hero" let:firstName let:lastName>{firstName} {lastName}</h4>
  </Names>
  <Names>
    <h4 slot="hero" let:firstName let:lastName>{lastName} {firstName}</h4>
  </Names>
  <Names>
    <h4 slot="hero" let:firstName>{firstName}</h4>
  </Names> -->

  <!-- <h3>App component global style</h3>
  <h4>App component local style</h4>
  <ChildStyles /> -->

  <!-- <PostList /> -->

  <!-- <AutoFocus /> -->

  <!-- <Dynamic /> -->

  <!-- why this is not working? -> variables defined in the module scripts are not reactive -->
  <!-- <h3>Total Count: {getTotalCount()}</h3> -->
  <button on:click={() => alert(getTotalCount())}>Get Total Count</button>
  <Counter />
  <Counter />
  <Counter />
</main>

<style>
  /* :global(h3) {
    color: red;
  } */

  /* h4 {
    color: orange;
  } */
</style>
