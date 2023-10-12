<script>
  export let icon = "";
</script>

<template lang="pug">
  button
    i(class="{icon.substring(0,2)} {icon}")
    span
      slot
</template>

<style lang="scss">
  button {
    background: var(--sf-0);
    border-radius: 5px;
    padding: 4px 6px;
    &:hover {
      background: var(--ov-0);
    }
    :not(:last-child) {
      margin-right: 5px;
    }
  }
</style>
