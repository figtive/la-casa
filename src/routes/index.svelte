<script>
  import Logo from '$lib/Logo.svelte';
</script>

<div class="logo">
  <Logo />
  <div class="text">
    <div class="title-h1 fight">FIGHT</div>
    <div class="title-h2 interactive">interactive</div>
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
<span class="bogos">👽</span>

<style lang="scss">
  .logo {
    display: flex;
    flex-direction: row;
    align-items: center;
    .text {
      margin-left: 14px;
      .fight {
        font-size: 7.4rem;
        line-height: calc(7.4rem + 1rem);
      }
      .interactive {
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
    a {
      margin: 0 8px;
      color: #bbbbbb22;
      transition: 0.25s;
      :hover {
        color: #ff660055;
      }
    }
  }

  .bogos {
    position: absolute;
    opacity: 0.05;
    bottom: 5vh;
  }
</style>
