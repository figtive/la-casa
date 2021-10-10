<div class="main-container">
  <main>
    <slot />
  </main>
</div>

<style lang="scss" global>
  .main-container {
    background-color: #222;
    position: relative;
    width: 100%;
    height: 100%;
    color: #333;
    box-sizing: border-box;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue',
      sans-serif;
    main {
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      user-select: none;
    }
  }

  .title {
    font-family: 'Urbanist', sans-serif;
    margin: 0;
    &-h1 {
      @extend .title;
      color: #ff6600;
      font-size: 4rem;
      font-weight: 700;
    }
    &-h2 {
      @extend .title;
      color: #bbb;
      font-size: 3rem;
      font-weight: 300;
    }
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
