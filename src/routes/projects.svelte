<script context="module" lang="ts">
  /**
   * @type {import('@sveltejs/kit').Load}
   */
  export async function load({ fetch }) {
    const res = await fetch('https://api.github.com/orgs/figtive/repos?sort=pushed', { credentials: 'omit' });
    if (res.ok) {
      return {
        props: {
          projects: await res.json(),
        },
        maxage: 60 * 30,
      };
    }
    return {
      props: {
        error: `Could not load projects!${res.statusText && ` (${res.statusText})`}`,
      },
    };
  }
</script>

<script lang="ts">
  import Title from '$lib/Title.svelte';
  export let projects = [];
  export let error = '';
</script>

<Title title="Projects" description="Fight Interactive's projects" />

<div class="main">
  <h1 class="title-h1">Projects</h1>
  {#if error}
    <div class="alert-error">{error}</div>
    <div class="alert-info">
      Check out our <a href="https://github.com/figtive" target="_blank" rel="noopener" class="link">GitHub</a> instead!
    </div>
  {/if}
  {#each projects as project (project.id)}
    <div class="project">
      <p>
        <a class="link" href={project.html_url} target="_blank" rel="noopener">{project.full_name}</a>
      </p>
      <p class="tag-list">
        {#each project.topics as tag (tag)}
          <span class="tag">{tag}</span>
        {/each}
      </p>
      <p>{project.description}</p>
    </div>
  {/each}
</div>

<style lang="scss">
  .link {
    line-height: 1.8rem;
  }

  .project {
    margin-bottom: 32px;
    p {
      margin: 0;
    }
    .tag-list {
      margin-top: 2px;
      margin-bottom: 4px;
      .tag {
        color: #eee;
        font-size: 0.8rem;
        line-height: 1.8rem;
        border: 1px solid $color-primary;
        padding: 2px 8px;
        border-radius: 16px;
        background-color: transparentize($color: $color-primary, $amount: 0.85);
        margin-right: 8px;
        &:last-child {
          margin-right: 0;
        }
      }
    }
  }
</style>
