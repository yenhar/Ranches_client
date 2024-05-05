<template>
    <navigation/>
    <div class="contact container mx-auto">
      <h1>Contact Us</h1>
      <p>Get in touch with us using the form below.</p>
      <form @submit.prevent="handleSubmit">
        <div class="form-group">
          <label for="name">Name</label>
          <textbox/>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <textbox/>
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textbox/>
        </div>
        <button type="button" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded mt-8">
      Send Message
    </button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        email: '',
        message: '',
      };
    },
    methods: {
      handleSubmit(event) {
        // Handle form submission logic (e.g., validation, sending data)
        event.preventDefault(); // Prevent default form submission behavior
        console.log('Form submitted:', this.name, this.email, this.message);
        // Implement your desired form submission handling here (API call, email, etc.)
  
        // Example: Reset form after successful submission
        this.name = '';
        this.email = '';
        this.message = '';
      },
    },
  };
  </script>
  
  <style scoped>
  .contact {
    padding: 2rem;
  }
  .form-group {
    margin-bottom: 1rem;
  }
  /* Add other styles as needed */
  </style>