<!-- OrganizerPage.svelte -->
<script>
 
</script>

<div class="page">
  

  <div class="right-column">
    <div class="content">
      <h2>Organizers List </h2>
    </div>
  </div>
</div>

<style>
  .page {
    background-color: rgba(34, 34, 34, 0.9); /* Use the global background color with transparency */
    display: flex;
    flex-direction: row; /* Arrange elements in a row */
    align-items: flex-start; /* Align elements at the top */
  }


  .right-column {
    flex: 1; /* Allow the right column to take remaining width */
    padding: 20px; /* Add padding to the right column */
  }

  .left-panel {
    background-color: #ddd; /* Set background color of the left panel */
    height: 100%; /* Occupy full height of the left column */
  }

  .content {
    background-color: #fff; /* Set background color of the content */
    /* Add other styles for the content area */
  }

  /* Define additional styles for .tab, .page, .left-column, .right-column, .left-panel, .content, etc. as needed */
</style>

