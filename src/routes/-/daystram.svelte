<script lang="ts">
  import Title from '$lib/Title.svelte';
</script>

<Title title="daystram" description="Danny August Ramaputra" />

<iframe src="https://daystram.com" title="daystram" id="daystram-iframe" />

<style>
  #daystram-iframe {
    position: fixed;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    width: 100%;
    height: 100%;
    border: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
  }
</style>
