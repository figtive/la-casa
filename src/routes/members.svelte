<script lang="ts">
  import Title from '$lib/Title.svelte';

  // lexicographic order on the username
  const members: { name: string; username: string }[] = [
    {
      name: 'Danny August Ramaputra',
      username: 'daystram',
    },
    {
      name: 'Muhamad Ilman Nafian',
      username: 'ilman',
    },
    {
      name: 'Muhammad Naufal Irbahhana',
      username: 'irbahhana',
    },
    {
      name: 'Nicolaus Christian Gozali',
      username: 'nicolauscg',
    },
    {
      name: 'Wahyu Ananda Duli Tokan',
      username: 'wahyuadt',
    },
  ];
</script>

<Title title="Members" description="Fight Interactive members" />

<div class="main">
  <h1 class="title-h1">Members</h1>
  <table>
    <tbody>
      {#each members as member}
        <tr>
          <td>
            <a target="_blank" rel="noopener" href="/-/{member.username}" class="link">{member.username}</a>
          </td>
          <td> {member.name}</td>
        </tr>
      {/each}
    </tbody>
  </table>
</div>

<style lang="scss">
  td {
    padding-bottom: 32px;
    &:first-child {
      padding-right: 32px;
    }
  }
</style>
