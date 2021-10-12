<script lang="ts">
  import Title from '$lib/Title.svelte';

  const members = [
    {
      name: 'Danny August Ramaputra',
      username: 'daystram',
    },
    {
      name: 'Wahyu Ananda Duli Tokan',
      username: 'wahyuadt',
    },
    {
      name:'Muhammad Naufal Irbahhana',
      username: 'irbahhana'
    }
  ];
</script>

<Title title="Members" description="Fight Interactive members" />

<div class="main">
  <div class="container mx-auto">
    <h1 class="title-h1">Members</h1>
    <table class="table-auto list">
      <tbody>
        {#each members as member (member.username)}
          <tr>
            <td class="pr-8">
              <a target="_blank" rel="noopener" href="/-/{member.username}" class="link">{member.username}</a>
            </td>
            <td> {member.name}</td>
          </tr>
        {/each}
      </tbody>
    </table>
  </div>
</div>

<style lang="scss">
  td {
    height: 3rem;
  }
</style>
