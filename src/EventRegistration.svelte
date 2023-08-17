<!-- EventRegistration.svelte -->
<script>
    // ... imports ...
  
    let organizers = []; // Populate this array with organizer data
    let ticketTypes = ["General", "VIP", "Premium"]; // Example ticket types
  
    let eventName = "";
    let selectedOrganizer = null;
    let selectedTicketType = ticketTypes[0];
  
    // ... event handlers ...
  
    function handleEventCreation() {
      // Perform event creation logic here
    }
  
    // ... other code ...
  
  </script>
  
  <div class="form-container">
    <h2>Add Event</h2>
    <form on:submit|preventDefault={handleEventCreation}>
      <div class="form-group">
        <label for="event-name">Event Name</label>
        <input type="text" id="event-name" bind:value={eventName} />
      </div>
      <div class="form-group">
        <label for="organizer">Select Organizer</label>
        <select id="organizer" bind:value={selectedOrganizer}>
          {#each organizers as organizer}
            <option value={organizer.id}>{organizer.name}</option>
          {/each}
        </select>
      </div>
      <div class="form-group">
        <label for="ticket-type">Select Ticket Type</label>
        <select id="ticket-type" bind:value={selectedTicketType}>
          {#each ticketTypes as type}
            <option value={type}>{type}</option>
          {/each}
        </select>
      </div>
      <div class="form-group">
        <!-- Other form fields for event details ... -->
      </div>
      <div class="form-group">
        <button class="submit-button" type="submit">Create event</button>
      </div>
    </form>
  </div>
  
  <style>
  

  .form-container {
    background-color: rgba(34, 34, 34, 0.9); /* Use the global background color with transparency */
    padding: 20px;
    border-radius: 10px;
    margin: 20px auto;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    color: white;
  }

  .form-container h2 {
    margin-bottom: 20px;
    font-size: 1.5rem;
    color: #fff;
  }

  /* Form Groups */
  .form-group {
    margin-bottom: 15px;
  }

  /* Labels */
  label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
  }

  /* Input Fields and Select */
  input[type="text"],
  select {
    width: 70%;
    padding: 10px;
    border: none;
    border-radius: 5px;
    background-color: rgba(255, 255, 255, 0.1);
    color: white;
    margin-top: 5px;
  }
  option {
    color: black; /* Change to the appropriate color for better visibility */
  }

  /* Submit Button */
  .submit-button {
    background-color: #2196f3;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    transition: background-color 0.3s;
  }

  .submit-button:hover {
    background-color: #0d8bf0;
  }

  </style>
  