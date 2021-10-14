<script lang="ts">
  import Logo from '$lib/Logo.svelte';
  import { page } from '$app/stores';
  import { fly } from 'svelte/transition';
</script>

<nav class="navbar">
  <div class="navbar-container">
    {#if $page.path !== '/'}
      {#key $page.path}
        <div class="navbar-brand" in:fly={{ x: -4, duration: 500 }} out:fly={{ x: 4, duration: 500 }}>
          <a href="/">
            <Logo />
          </a>
        </div>
      {/key}
    {/if}
    <div class="flex-grow" />
    <a href="/projects" class="navbar-item">Projects</a>
    <a href="/members" class="navbar-item">Members</a>
    <a href="/about-us" class="navbar-item">About Us</a>
  </div>
</nav>

<style lang="scss">
  .navbar {
    position: absolute;
    top: 0;
    width: 100%;
    height: 64px;
    z-index: 2000;
    background-color: transparent;
    opacity: 0.8;
    &-container {
      height: inherit;
      padding: 0 32px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    &-brand {
      width: calc(64px - 32px);
    }
    &-item {
      color: $color-primary;
      font-family: 'Urbanist', sans-serif;
      font-size: 1.2rem;
      text-transform: uppercase;
      font-weight: 800;
      text-decoration: none;
      position: relative;
      margin-left: 24px;
      &:first-of-type {
        margin-left: 0;
      }
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
        top: -2px;
        bottom: -2px;
        left: -2px;
        width: 0;
        transition: 0.5s $transition-default;
        background: $color-primary;
        mix-blend-mode: difference;
      }
    }
  }
</style>
