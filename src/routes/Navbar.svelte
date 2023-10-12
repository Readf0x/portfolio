<script>   import { page } from "$app/stores";
</script>

<template lang="pug">
  nav.navigation
    a.logo(
      href="/"
      aria-current!="{$page.url.pathname === '/' ? 'page' : undefined}"
    ) #[img(src="/favicon-invert.svg" alt="logo")] Davis Forsythe
    a(
      href="/about"
      aria-current!="{$page.url.pathname === '/about' ? 'page' : undefined}"
    ) #[i.nf.nf-oct-info] About Me
</template>

<style lang="scss">
  .navigation {
    display: flex;
    height: 48px;
    align-items: center;
    gap: 5px;
    padding: 0 10px;
    border-bottom: 2px solid transparent;
    // box-sizing: border-box;
    :nth-child(2) {
      margin-left: auto;
    }
    a {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 5px;
      text-decoration: none;
      color: inherit;
      font-size: 18px;
      height: calc(100% + 2px);
      padding: 0 10px;
      border-bottom: 2px solid transparent;
      &:hover {
        color: var(--text-1);
        border-bottom-color: var(--ov-2) !important;
      }
      &[aria-current='page'] {
        border-bottom-color: var(--accent);
      }
      &.logo {
        font-size: 20px;
        img {
          height: 0.9em;
          position: relative;
         ;top: 1px;
          color: var(--text-2);
        }
      }
    }
  }
</style>
