<script>
  import UserName from "./UserName.svelte";

  export let name = "Sushanth";
  export let superHeroName = "Superman";
</script>

<p>
  Hello <b>
    {name}
  </b>
  a.k.a
  <b>
    {superHeroName}
  </b>
  by
  <UserName />
</p>
