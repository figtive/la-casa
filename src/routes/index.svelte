<script>
  import Logo from '$lib/Logo.svelte';
</script>

<div class="main-container">
  <main>
    <div class="title">
      <Logo />
      <h1 class="title-text">
        <div class="title-p1">FIGHT</div>
        <div class="title-p2">interactive</div>
      </h1>
    </div>
    <div class="links">
      <a href="https://github.com/figtive" aria-label="GitHub" target="_blank" rel="noopener">
        <i class="fab fa-github-square" />
      </a>
      <a href="https://twitter.com/figtive" aria-label="Twitter" target="_blank" rel="noopener">
        <i class="fab fa-twitter-square" />
      </a>
      <a href="https://steamcommunity.com/groups/figtive" aria-label="Steam" target="_blank" rel="noopener">
        <i class="fab fa-steam-square" />
      </a>
    </div>
    <span class="bogos">👽</span>
  </main>
</div>

<style>
  .main-container {
    background-color: #222;
    position: relative;
    width: 100%;
    height: 100%;
    color: #333;
    box-sizing: border-box;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue',
      sans-serif;
  }
  main {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    user-select: none;
  }
  .title {
    display: flex;
    justify-content: center;
  }
  .title-text {
    font-family: 'Urbanist', sans-serif;
    font-size: 3.7em;
    margin: 0;
    margin-left: 14px;
  }
  .title-p1 {
    color: #ff6600;
    font-size: 2em;
    font-weight: 700;
    line-height: 1em;
  }
  .title-p2 {
    padding-left: 0.05em;
    color: #bbb;
    font-weight: 300;
    font-size: 1.2em;
    line-height: 0.5em;
  }
  .links {
    margin-top: 32px;
    font-size: 2em;
  }
  .links a {
    margin: 0 8px;
    color: #bbbbbb22;
    transition: 0.25s;
  }
  .links a:hover {
    color: #ff660055;
  }
  .bogos {
    position: absolute;
    opacity: 0.05;
    bottom: 5vh;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
