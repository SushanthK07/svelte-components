<script>
  const names = [
    {
      firstName: "Virat",
      lastName: "Kohli",
    },
    {
      firstName: "Sachin",
      lastName: "Tendulkar",
    },
    {
      firstName: "MS",
      lastName: "Dhoni",
    },
  ];
</script>

<h2>Names</h2>
{#each names as name (name)}
  <!-- <p>{name.firstName} {name.lastName}</p> -->
  <slot name="hero" firstName={name.firstName} lastName={name.lastName} />
{/each}
