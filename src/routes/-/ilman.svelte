<script lang="ts">
  // just for future proofing when we decided to use ssr and serve static content from elsewhere
  import { assets } from '$app/paths';
</script>

<div class="wrapper">
  <img src="{assets}/ilman/stare.jpg" alt="me" height="200px" width="200px" />
  <p class="emoji">👉</p>
  <a href="https://github.com/ilmannafian04" aria-label="GitHub" target="_blank" rel="noopener">
    <i class="fab fa-github emoji" />
  </a>
</div>

<style>
  .wrapper {
    background-color: #0d1117;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    color: whitesmoke;
    column-gap: 20px;
  }
  .emoji {
    font-size: 10em;
  }
</style>
