<script>
  export let title;
  export let description =
    'Fight Interactive is a team of developers who are passionate about creating interactive experiences for everyone.';
</script>

<svelte:head>
  <title>{title}{title && ' / '}Fight Interactive</title>
  <meta name="description" content={description} />
</svelte:head>
