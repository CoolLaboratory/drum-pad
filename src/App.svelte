<script lang="ts">
  import Pad from "./lib/Pad.svelte";
  import {
    clapIcon,
    closedHihatIcon,
    crashIcon,
    kickIcon,
    openHihatIcon,
    snareIcon,
  } from "./assets/icons/index";

  let padContainer: HTMLElement
</script>

<header style="display:flex; text-align:end; padding:10px;">
  <div style="display:inline-flex; flex:1; align-items:center; justify-content: flex-start;">
    <span>Simple DrumPad</span>
  </div>

  <div style="display:inline-flex; flex:1; justify-content:flex-end;">
    <button 
      style="display:inline-grid; place-items:center; aspect-ratio: 1; cursor:pointer;"
      on:click={() => padContainer.requestFullscreen()}
    >
      <svg viewBox="0 0 24 24" width="24" height="24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round" class="css-i6dzq1"><path d="M8 3H5a2 2 0 0 0-2 2v3m18 0V5a2 2 0 0 0-2-2h-3m0 18h3a2 2 0 0 0 2-2v-3M3 16v3a2 2 0 0 0 2 2h3"></path></svg>
    </button>
  </div>
  
    
</header>

<main bind:this={padContainer}>
  <Pad icon={clapIcon} sound={"clap"} />
  <Pad icon={crashIcon} sound={"crash"} />
  <Pad icon={openHihatIcon} sound={"openHihat"} />
  <Pad icon={kickIcon} sound={"kick"} />
  <Pad icon={snareIcon} sound={"snare"} />
  <Pad icon={closedHihatIcon} sound={"closedHihat"} />
</main>

<style>
  main {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);
    gap: 10px;
    block-size: 100vh;
    padding: 10px;
    box-sizing: border-box;
  }
  /* .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  } */
</style>
