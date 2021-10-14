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
        maxage: 60 * 60,
      };
    }
    return {
      error: new Error(`Could not load projects! (${res.statusText})`),
    };
  }
</script>

<script lang="ts">
  import Title from '$lib/Title.svelte';
  export let projects = [];
</script>

<Title title="Projects" description="Fight Interactive's projects" />

<div class="main">
  <div class="container mx-auto px-4">
    <h1 class="title-h1">Projects</h1>
    {#each projects as project (project.id)}
      <div class="mb-8">
        <a class="link" href={project.html_url} target="_blank" rel="noopener">{project.full_name}</a>
        <p>
          {#each project.topics as tag (tag)}
            <span class="tag">{tag}</span>
          {/each}
        </p>
        <p>{project.description}</p>
      </div>
    {/each}
  </div>
</div>

<style lang="scss">
  .link {
    font-weight: 600;
    line-height: 1.8rem;
  }

  .tag {
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
</style>
