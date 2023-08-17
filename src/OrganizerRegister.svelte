<!-- OrganizerForm.svelte -->
<script>
    let organizerName = '';
    let email = '';
    let phone = '';
  
    function handleSubmit() {
      // Handle form submission here
      // You can send the data to your backend or perform any other action
      console.log('Form submitted:', { organizerName, email, phone });
    }
  </script>
  
  <div class="form-container">
    <h2>Register Organizer</h2>
    <form>
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" id="name" name="name" placeholder="Enter your name" />
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" name="email" placeholder="Enter your email" />
      </div>
      <div class="form-group">
        <label for="phone">Phone</label>
        <input type="tel" id="phone" name="phone" placeholder="Enter your phone number" />
      </div>
      <div class="form-group">
        <label for="company">Company</label>
        <input type="text" id="company" name="company" placeholder="Enter your company name" />
      </div>
      <button class="submit-button" type="submit">Register</button>
    </form>
  </div>
  
  <style>
  .form-container {
    background-color: rgba(34, 34, 34, 0.9); /* Use the global background color with transparency */
    padding: 20px;
    border-radius: 10px;
    margin-top: 20px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    color: white; /* Text color for form labels and input */
  }

  .form-container h2 {
    margin-bottom: 20px;
    font-size: 1.5rem;
    color: #fff; /* Heading color */
  }

  .form-group {
    margin-bottom: 15px;
  }

  label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
  }

  input {
    width: 70%;
    padding: 10px;
    border: none;
    border-radius: 5px;
    background-color: rgba(255, 255, 255, 0.1); /* Slightly transparent background */
    color: white; /* Text color */
    margin-top: 5px;
  }

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
  