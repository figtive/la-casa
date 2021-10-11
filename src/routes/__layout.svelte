<script lang="ts">
  import Navbar from '$lib/Navbar.svelte';
  import '../tailwind.css';
</script>

<Navbar />

<div class="root-container">
  <slot />
</div>

<style lang="scss" global>
  .root-container {
    background-color: $color-background;
    position: relative;
    width: 100%;
    min-height: 100vh;
    box-sizing: border-box;
  }

  .main {
    padding-top: $navbar-height;
    min-height: calc(100vh - $navbar-height);
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue',
      sans-serif;
    color: $color-secondary;

    h1 {
      margin-bottom: 3rem;
    }

    .title {
      font-family: 'Urbanist', sans-serif;
      margin: 0;
      &-h1 {
        @extend .title;
        color: $color-primary;
        font-size: 4rem;
        font-weight: 700;
        text-transform: uppercase;
      }
      &-h2 {
        @extend .title;
        color: $color-secondary;
        font-size: 3rem;
        font-weight: 300;
      }
    }

    i {
      color: inherit;
    }

    .link {
      color: $color-primary;
      text-decoration: none;
      position: relative;
      &:hover {
        text-decoration: none;
        &::before {
          width: calc(100% + 4px);
        }
      }
      &::before {
        content: '';
        display: block;
        position: absolute;
        height: 0.1em;
        bottom: -2px;
        left: -2px;
        width: 0;
        transition: 0.5s cubic-bezier(0.75, 0.75, 0.25, 1);
        background: $color-primary;
      }
    }
  }
</style>
