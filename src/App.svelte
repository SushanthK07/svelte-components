<script>
  import Greet from "./components/Greet.svelte";

  const name = "Modi";
  const superHeroName = "Prime Minister of India";

  const person = {
    name: "Virat Kohli",
    superHeroName: "GOAT",
  };
</script>

<main>
  <Greet superHeroName="HanuMan" />
  <Greet name="Phaneendra" superHeroName="IronMan" />
  <Greet name="Krishna" />
  <Greet {name} {superHeroName} />
  <Greet {...person} />
</main>

<style>
</style>
