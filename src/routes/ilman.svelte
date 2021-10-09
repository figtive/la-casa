<script lang="ts">
  // just for future proofing when we decided to use ssr and serve static content from elsewhere
  import { assets } from '$app/paths';
  import Divider from '$lib/ilman/Divider.svelte';
</script>

<div class="container">
  <img src="{assets}/ilman/stare.jpg" alt="me" height="200px" width="200px" />
  <Divider />
  <div>
    <p>asdasd</p>
    <p>asdasd</p>
  </div>
</div>

<style>
  .container {
    background-color: #0d1117;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    color: whitesmoke;
    column-gap: 20px;
  }
</style>
