<script>
  import Logo from '$lib/Logo.svelte';
</script>

<div class="main">
  <div class="logo">
    <div class="logo-icon">
      <Logo />
    </div>
    <div class="logo-text">
      <div class="title-h1 logo-text-fight">FIGHT</div>
      <div class="title-h2 logo-text-interactive">interactive</div>
    </div>
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
</div>
<span class="bogos">👽</span>

<style lang="scss">
  .main {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    // override default navbar padding for index page
    padding-top: 0;
    height: 100vh;
  }
  .logo {
    display: flex;
    flex-direction: row;
    align-items: center;
    user-select: none;
    &-icon {
      width: 128px;
      height: 174px;
    }
    &-text {
      margin-left: 14px;
      &-fight {
        font-size: 7.4rem;
        line-height: calc(7.4rem + 1rem);
      }
      &-interactive {
        font-size: 4.44rem;
        line-height: calc(4.44rem + 1rem);
        margin-top: -2rem;
        padding-left: 4px;
      }
    }
  }

  .links {
    margin-top: 32px;
    font-size: 2rem;
    display: flex;
    justify-content: center;
    a {
      margin: 0 8px;
      color: transparentize($color: $color-secondary, $amount: 0.75);
      transition: 0.25s;
      :hover {
        color: transparentize($color: $color-primary, $amount: 0.5);
      }
    }
  }

  .bogos {
    position: absolute;
    opacity: 0.05;
    bottom: 5vh;
    width: 100%;
    text-align: center;
  }
</style>
