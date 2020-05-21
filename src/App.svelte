<script lang="typescript">
  import { darkMode } from "./stores/darkMode.js";
  import { media } from "./stores/watchMedia.js";
  import "./CSS/tailwind.css";

  let title: string = " from Typescript";
</script>

<main class="h-screen bg-red-500 dark:bg-blue-500">
  {#if $media.md}
    <h1 class="text-white">Hello{title}</h1>
  {:else}
    <h1 class="text-white">Bye{title}</h1>
  {/if}
  <button on:click={() => ($darkMode ? darkMode.turnOff() : darkMode.turnOn())}>
    darkmode
  </button>
</main>
