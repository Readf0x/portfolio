<script>
  import Header from "./Header.svelte";
  export let data;
  let { hello } = data;
</script>

<template lang="pug">
  Header(hello!="{JSON.stringify(hello)}")
</template>

<svelte:head>
  <title>Davis Forsythe</title>
</svelte:head>
