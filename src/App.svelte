<script>
  import Logo from './components/Logo.svelte';
</script>

<main>
  <div class="title">
    <Logo />
    <div class="title-text">
      <div class="title-p1">FIGHT</div>
      <div class="title-p2">interactive</div>
    </div>
  </div>
</main>

<style>
  main {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
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

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
