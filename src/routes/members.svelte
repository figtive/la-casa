<script lang="ts">
  import Title from '$lib/Title.svelte';

  const members = [
    {
      name: 'Danny August Ramaputra',
      username: 'daystram',
      path: 'daystram',
    },
    {
      name: 'Wahyu Ananda Duli Tokan',
      username: 'wahyuadt',
      path: 'wahyuadt',
    },
  ];
</script>

<Title title="Members" />

<div class="main">
  <div class="container mx-auto">
    <h1 class="title-h1">Members</h1>
    <ul>
      {#each members as member (member.path)}
        <li class="mb-4">{member.name} <a href="/-/{member.path}" class="link">{member.username}</a></li>
      {/each}
    </ul>
  </div>
</div>
