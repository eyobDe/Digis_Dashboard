<!-- LeftPanel.svelte -->
<script>
  import { navigate } from 'svelte-routing';
  export let activeTab;
</script>

<div class="left-panel">
  <div class="logo">
    <img src="https://svelte.dev/svelte-logo-horizontal.svg" alt="Svelte Logo" />
  </div>
  <div class="tab" on:click={() => navigate('/organizers')} class:selected={activeTab === '/organizers'}>
    Organizers
  </div>
  <div class="tab" on:click={() => navigate('/events')} class:selected={activeTab === '/events'}>
    Events
  </div>
  <!-- Add more tabs for other functionalities -->
</div>

<style>
   .left-panel {
    width: 250px;
    background-color: #333;
    color: white;
    /* Updated styles for height and scrolling */
    height: 100vh; /* Extend height to viewport height */
    overflow-y: auto; /* Enable vertical scrolling */
    display: flex;
    flex-direction: column;
    padding: 20px;
  }

  .logo {
    padding-bottom: 20px; /* Add spacing below the logo */
    text-align: center;
  }

  .logo img {
    max-width: 100%;
  }

  .tab {
    padding: 10px;
    cursor: pointer;
  }

  .tab.selected {
    background-color: #444;
  }
</style>
