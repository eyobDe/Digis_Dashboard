<!-- App.svelte -->
<script>
	import { onMount, onDestroy } from 'svelte';
	
	import { Router, Route,  navigate} from "svelte-routing";
	import LeftPanel from './LeftPanel.svelte';
	import OrganizerPage from './OrganizerPage.svelte';
	import EventPage from './EventPage.svelte';
    import OrganizerRegisteration from "./OrganizerRegister.svelte"; // Import the RegisterOrganizer component
	import EventRegistration from "./EventRegistration.svelte"; // Import the EventRegistration component


	let activeTab = '/organizers';
  
	// Handle route change logic here...
  
	onMount(() => {
	  // Add event listener for route change...
	});
  
	onDestroy(() => {
	  // Remove event listener on component cleanup...
	});
  
	// Event handlers for menu buttons
	function handleAddOrganizer() {
    // Programmatically navigate to the RegisterOrganizer page
	navigate("/register-organizer");
  }
  function handleAddEvent() {
    navigate("/add-event");
  }
  
	function handleAddUser() {
	  // Handle Add User action here...
	}
  </script>
  
  <main>
	<div class="app-container">
	  <!-- Original LeftPanel -->
	  <LeftPanel activeTab={activeTab} />
  
	  <!-- New Left Side Panel with Tabs -->
	  
  
	  <!-- Content Area -->
	  <div class="content">
		<!-- Menu Buttons -->
		<div class="horizontal-menu">
			<button class="menu-button add-organizer" on:click={handleAddOrganizer}>Add Organizer</button>
			<button class="menu-button add-event" on:click={handleAddEvent}>Add Event</button>
			<button class="menu-button add-user" on:click={handleAddUser}>Add User</button>
		  
		</div>
	
  
		<!-- Page Content -->
		<Router>
		  <Route path="/organizers" component={OrganizerPage} />
		  <Route path="/events" component={EventPage} />
		  <Route path="/register-organizer" component={OrganizerRegisteration} /> <!-- Add this route -->
		  <Route path="/add-event" component={EventRegistration} /> <!-- Add this route -->
     
		  <!-- ... other routes ... -->
		</Router>
	  </div>
	</div>
  </main>
  
  
  <style>
	:global(body) {
    background-color: #222; /* Use the desired color */
    margin: 0;
    font-family: sans-serif;
  }
	.app-container {
	  display: flex;
	  flex-direction: row;
	}
  
	.tabs-panel {
	  width: 250px;
	  background-color: #f0f0f0;
	  padding: 20px;


	  
	}


  
	.tab {
	  padding: 10px;
	  cursor: pointer;
	}
  
	.left-panel {
	  width: 250px;
	  background-color: #333;
	  color: white;
	  display: flex;
	  flex-direction: column;
	  padding: 20px;
	}
  
	.content {
	  flex: 1;
	  padding: 20px;
	}
	.horizontal-menu {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center; /* Align items in the center horizontally */
    background-color: #333;
    padding: 10px;
    border-radius: 10px;
    margin-bottom: 20px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
	.menu {
    display: flex;
    justify-content: center; /* Align buttons in the center horizontally */
    padding: 10px 0; /* Add some vertical spacing */
  }

  .menu-button {
    margin: 0 10px; /* Add horizontal spacing between buttons */
    padding: 10px 20px;
    border: none;
    border-radius: 10px;
    cursor: pointer;
    font-weight: bold;
    color: white;
  }

  .add-organizer {
    background-color: #4caf50; /* Green */
  }

  .add-event {
    background-color: #2196f3; /* Blue */
  }

  .add-user {
    background-color: #f44336; /* Red */
  }
	/* Define additional styles for .tab, .app-container, .tabs-panel, .left-panel, .content, etc. as needed */
  </style>
  
  