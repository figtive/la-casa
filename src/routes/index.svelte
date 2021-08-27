<script>
  import Logo from '$lib/Logo.svelte';
</script>

<main>
  <div class="title">
    <Logo />
    <div class="title-text">
      <div class="title-p1">FIGHT</div>
      <div class="title-p2">interactive</div>
    </div>
  </div>
  <div class="links">
    <a href="https://github.com/figtive" target="_blank" rel="noopener">
      <i class="fab fa-github" />
    </a>
    <a href="https://steamcommunity.com/groups/figtive" target="_blank" rel="noopener">
      <i class="fab fa-steam" />
    </a>
  </div>
  <div class="bogos">👽</div>
</main>

<style>
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
