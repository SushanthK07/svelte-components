<script>
  import { onMount } from "svelte";

  let posts = [];
  console.log(posts);

  onMount(async () => {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts");
    posts = await response.json();
    console.log(posts);
  });
</script>

<main>
  <h2>Posts:</h2>
  <ul>
    {#each posts as post (post.id)}
      <li>
        <h3>{post.title}</h3>
        <p>{post.body}</p>
        <hr />
      </li>
    {:else}
      <p>Loading...</p>
    {/each}
  </ul>
</main>
