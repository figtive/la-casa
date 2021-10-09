<div class="container">
  {#each Array(3) as _, i (i)}
    <span class="dot" />
  {/each}
</div>

<style>
  .container {
    display: flex;
    flex-direction: column;
    row-gap: 30px;
  }

  .dot {
    background-color: #33cb56;
    border-radius: 50%;
    height: 15px;
    width: 15px;
  }
</style>
