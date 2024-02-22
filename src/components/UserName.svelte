<script>
  import { getContext } from "svelte";
  const userInfo = getContext("user-info");
</script>

<b>{userInfo.name}</b>
