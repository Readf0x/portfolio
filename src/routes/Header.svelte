<script>
  import { onMount } from "svelte";
  import background from "$lib/images/header.svg";
  import headshot from "$lib/images/Headshot-og.jpg";

  /** * @type {string}*/
   export let hello;
   hello = JSON.parse(hello);
</script>

<template lang="pug">
  .header
    .text
      h1 
        span.greeting(title!="{hello[1]}") {hello[0]}
        |, I'm #[br] Davis Forsythe
      p Learning programming one step at a time
    img(src="{headshot}" alt="header")
</template>

<style lang="scss">
  @import "@catppuccin/palette/scss/mocha";

  .header {
    height: 40vw;
    max-height: 60vh;
    display: flex;
    padding: 15px 0;
    justify-content: space-around;
    align-items: center;
    background: var(--bg-1);
    .text {
      text-align: center;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding-bottom: 4vh;
      width: 45vw;
      h1 {
        font-size: 6vw;
        background: linear-gradient(to bottom right, $sapphire, $red);
        -webkit-background-clip: text;
        background-clip: text;
        -webkit-text-fill-color: transparent;
        .greeting {
          border-bottom: 0.5vw dashed var(--ov-0);
        }
      }
      p {
        font-size: 2vw;
      }
    }
    img {
      background: var(--ov-0);
      border-radius: 20px;
      height: calc(100% - 2vw);
      box-shadow: 1vw 1vw var(--ov-0), -1vw -1vw var(--bg-0);
    }
  }

  @media (max-aspect-ratio: 4/5) {
    .header {
      flex-direction: column;
      max-height: unset;
      height: fit-content;
      padding: 0 5%;
      .text {
        h1 {
          font-size: 10vw;
        }
        p {
          font-size: 5vw;
        }
      }
      img {
        margin: 0 10%;
        width: 100%;
      }
    }
  }

  @media (min-aspect-ratio: 4/3) {
    .header {
      max-width: 400vw;
      .text {
        h1 {
          font-size: 5vw;
        }
        p {
          font-size: 1.5vw;
        }
      }
    }
  }
</style>
