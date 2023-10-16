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
    ) About Me
</template>

<style lang="scss">
  .navigation {
    display: flex;
    height: 50px;
    align-items: center;
    gap: 5px;
    padding: 0 10px;
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
      &:hover {
        color: var(--text-1);
      }
      &[aria-current='page']:not(.logo) {
        color: var(--ac-0);
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

  // Mobile
  @media (max-aspect-ratio: 4/5) {
    
  }

  // Tablet
  @media (max-aspect-ratio: 4/3) {

  }
</style>
