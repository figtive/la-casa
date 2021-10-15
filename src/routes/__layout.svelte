<script context="module" lang="ts">
  export const load = async ({ page }) => ({
    props: {
      key: page.path,
    },
  });
</script>

<script lang="ts">
  import Navbar from '$lib/Navbar.svelte';
  import RouteTransition from '$lib/RouteTransition.svelte';

  export let key;
</script>

<Navbar />

<div class="root-container">
  <RouteTransition refresh={key}>
    <slot />
  </RouteTransition>
</div>

<style lang="scss" global>
  .root-container {
    overflow: hidden;
    background-color: $color-background;
    position: relative;
    width: 100%;
    min-height: 100vh;
    box-sizing: border-box;
  }

  .main {
    padding-top: $navbar-height;
    padding-bottom: 128px;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue',
      sans-serif;
    color: $color-secondary;

    h1 {
      margin-bottom: 3rem;
    }

    .title {
      font-family: 'Urbanist', sans-serif;
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
      font-weight: 600;
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

    .alert {
      padding: 1rem;
      border-left: 8px solid;
      margin-bottom: 8px;
      &:last-child {
        margin-bottom: 0;
      }
      &-success {
        @extend .alert;
        $color: #4caf50;
        color: $color;
        background: transparentize($color, 0.9);
        border-color: $color;
      }
      &-info {
        @extend .alert;
        $color: #2196f3;
        color: $color;
        background: transparentize($color, 0.9);
        border-color: $color;
      }
      &-warning {
        @extend .alert;
        $color: #ff9800;
        color: $color;
        background: transparentize($color, 0.9);
        border-color: $color;
      }
      &-error {
        @extend .alert;
        $color: #f44336;
        color: $color;
        background: transparentize($color, 0.9);
        border-color: $color;
      }
    }
  }
</style>
