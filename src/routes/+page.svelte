<script>
  import { onMount } from 'svelte';

  let name = "Markus"; // Replace with your name or make dynamic if needed
  let currentPage = ""; // Initialize the current page variable

  // Function to set the current page based on the URL
  onMount(() => {
    currentPage = window.location.pathname === '/' ? 'home' : window.location.pathname.substring(1);
  });

  function showMessage() {
    alert("202210155@gordoncollege.edu.ph or eugenemarkusalop@gmail.com");
  }
</script>

<style>
  /* Overall body style for alignment */
  html, body {
    height: 100%; /* Ensure both html and body cover full height */
    margin: 0; /* Remove default margin */
    background-color: black; /* Set the entire background color to black */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    font-family: Arial, sans-serif; /* Default font */
    overflow: hidden; /* Prevent scrolling */
  }

  /* Navbar styles */
  .navbar {
    background-color: black; /* Navbar background color */
    padding: 1rem 0;
    width: 100%; /* Full width */
    display: flex; /* Use flexbox for layout */
    justify-content: space-between; /* Align items with space between */
    align-items: center; /* Center items vertically */
  }

  .navbar-logo {
    font-size: 1.5rem; /* Logo font size */
    color: white; /* Logo color */
    margin-left: 20px; /* Margin for left positioning */
  }

  .navbar ul {
    list-style-type: none;
    padding: 0;
    margin: 0; /* Remove default margin */
    display: flex; /* Change to flex for better responsiveness */
    flex-wrap: wrap; /* Allow items to wrap in smaller screens */
  }

  .navbar li {
    margin: 0 15px;
  }

  .navbar a {
    color: white; /* Text color for links */
    text-decoration: none;
    font-size: 1.2rem;
    display: flex;
    align-items: center; /* Align icon with text */
    transition: color 0.3s ease; /* Smooth transition for hover effect */
  }

  .navbar a:hover {
    color: #ff6347; /* Hover color */
  }

  /* Active link style */
  .active {
    font-weight: bold; /* Make the active link bold */
  }

  /* Welcome section styles */
  .welcome-section {
    text-align: center;
    background-color: black; /* Ensure welcome section has black background */
    padding: 8rem 1rem; /* Reduce padding for better fit */
    box-sizing: border-box; /* Ensure padding is accounted for in the element's total width/height */
    max-height: 100vh; /* Limit to viewport height */
    overflow: hidden; /* Ensure no scrolling */
  }

  h1 {
    font-size: 2.5rem;
    color: white; /* Heading color */
    margin: 0; /* Remove default margin */
    padding-top: 1rem; /* Optional: Adjust top padding */
  }

  p {
    font-size: 1.2rem;
    color: white; /* Default paragraph color */
  }

  /* Change paragraph color to blue if on the portfolio page */
  .portfolio-page p {
    color: blue; /* Set paragraph color to blue */
  }

  /* Icon styles */
  .icon-container {
    display: flex;
    justify-content: center;
    gap: 1.5rem; /* Space between icons */
    margin-top: 2rem; /* Space between icons and the h1 */
  }

  .icon-container svg {
    width: 2rem;
    height: 2rem;
    fill: white; /* Set icon color to white */
  }

  /* Footer styles */
  .footer {
    text-align: center; /* Center text in footer */
    padding: 2.5rem 0; /* Add padding */
    background-color: black; /* Set footer background color */
    color: white; /* Set footer text color */
    font-size: 1rem; /* Set footer font size */
  }

  /* Responsive styles */
  @media (max-width: 768px) {
    .navbar {
      justify-content: center; /* Center navbar items on smaller screens */
    }

    .navbar li {
      margin: 0 10px; /* Reduce margin */
    }

    h1 {
      font-size: 2rem; /* Smaller heading size for mobile */
    }

    p {
      font-size: 1rem; /* Smaller paragraph size for mobile */
    }

    .welcome-section {
      padding: 1rem; /* Adjust padding for mobile */
    }

    .footer {
      font-size: 0.9rem; /* Smaller footer font size for mobile */
    }
  }

  @media (max-width: 480px) {
    .navbar a {
      font-size: 1rem; /* Even smaller font size for extra small screens */
    }
  }
</style>

<div class="font-lato">
<!-- Navigation Bar -->
<div class="navbar svelte-orwpcc">
  <div class="navbar-logo"> &lt;/&gt; Markus Alop</div> <!-- Added logo on the left -->
  <ul class="svelte-orwpcc">
    <li class="svelte-orwpcc">
      <a href="/" class="{currentPage === 'home' ? 'active' : ''}">
        <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
          <path stroke="white" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m4 12 8-8 8 8M6 10.5V19a1 1 0 0 0 1 1h3v-3a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v3h3a1 1 0 0 0 1-1v-8.5"/>
        </svg>
        Home
      </a>
    </li>
    <li class="svelte-orwpcc">
      <a href="/portfolio" class="{currentPage === 'portfolio' ? 'active' : ''}">
        <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
          <path stroke="white" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13.5 8H4m0-2v13a1 1 0 0 0 1 1h14a1 1 0 0 0 1-1V9a1 1 0 0 0-1-1h-5.032a1 1 0 0 1-.768-.36l-1.9-2.28a1 1 0 0 0-.768-.36H5a1 1 0 0 0-1 1Z"/>
        </svg>
        Portfolio
      </a>
    </li>
    <li class="svelte-orwpcc">
      <a href="/about" class="{currentPage === 'about' ? 'active' : ''}">
        <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
          <path stroke="white" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 21a9 9 0 1 0 0-18 9 9 0 0 0 0 18Zm0 0a8.949 8.949 0 0 0 4.951-1.488A3.987 3.987 0 0 0 13 16h-2a3.987 3.987 0 0 0-3.951 3.512A8.948 8.948 0 0 0 12 21Zm3-11a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"/>
        </svg>
        About
      </a>
    </li>
    <li class="svelte-orwpcc">
      <a href="/contact" class="{currentPage === 'contact' ? 'active' : ''}">
        <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
          <path stroke="white" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.427 14.768 17.2 13.542a1.733 1.733 0 0 0-2.45 0l-.613.613a1.732 1.732 0 0 1-2.45 0l-1.838-1.84a1.735 1.735 0 0 1 0-2.452l.612-.613a1.735 1.735 0 0 0 0-2.452L9.237 5.572a1.6 1.6 0 0 0-2.45 0c-3.223 3.2-1.702 6.896 1.519 10.117 3.22 3.221 6.914 4.745 10.12 1.535a1.601 1.601 0 0 0 0-2.456Z"/>
        </svg>
        Contact
      </a>
    </li>
  </ul>
</div>

<!-- Welcome Section -->
<div class="welcome-section {currentPage === 'portfolio' ? 'portfolio-page' : ''}">
  <h1>Hi! 👋🏼</h1>
  <h1>I'm {name} Alop</h1>
  <h1>An IT Student in Gordon College!</h1>

  <!-- Icon Section -->
  <div class="icon-container">
    <!-- Replace these SVGs with the logos you want to add -->
    <button on:click={showMessage} class="bg-transparent border-none cursor-pointer">
      <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
        <path d="M2.038 5.61A2.01 2.01 0 0 0 2 6v12a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V6c0-.12-.01-.238-.03-.352l-.866.65-7.89 6.032a2 2 0 0 1-2.429 0L2.884 6.288l-.846-.677Z"/>
        <path d="M20.677 4.117A1.996 1.996 0 0 0 20 4H4c-.225 0-.44.037-.642.105l.758.607L12 10.742 19.9 4.7l.777-.583Z"/>
      </svg>      
    </button>
    <a href="https://github.com/MarkusAlop" target="_blank">
    <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
      <path fill-rule="evenodd" d="M12.006 2a9.847 9.847 0 0 0-6.484 2.44 10.32 10.32 0 0 0-3.393 6.17 10.48 10.48 0 0 0 1.317 6.955 10.045 10.045 0 0 0 5.4 4.418c.504.095.683-.223.683-.494 0-.245-.01-1.052-.014-1.908-2.78.62-3.366-1.21-3.366-1.21a2.711 2.711 0 0 0-1.11-1.5c-.907-.637.07-.621.07-.621.317.044.62.163.885.346.266.183.487.426.647.71.135.253.318.476.538.655a2.079 2.079 0 0 0 2.37.196c.045-.52.27-1.006.635-1.37-2.219-.259-4.554-1.138-4.554-5.07a4.022 4.022 0 0 1 1.031-2.75 3.77 3.77 0 0 1 .096-2.713s.839-.275 2.749 1.05a9.26 9.26 0 0 1 5.004 0c1.906-1.325 2.74-1.05 2.74-1.05.37.858.406 1.828.101 2.713a4.017 4.017 0 0 1 1.029 2.75c0 3.939-2.339 4.805-4.564 5.058a2.471 2.471 0 0 1 .679 1.897c0 1.372-.012 2.477-.012 2.814 0 .272.18.592.687.492a10.05 10.05 0 0 0 5.388-4.421 10.473 10.473 0 0 0 1.313-6.948 10.32 10.32 0 0 0-3.39-6.165A9.847 9.847 0 0 0 12.007 2Z" clip-rule="evenodd"/>
    </svg>
    </a>
    <a href="https://www.facebook.com/MEBautistaA" target="_blank">    
    <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
      <path fill-rule="evenodd" d="M13.135 6H15V3h-1.865a4.147 4.147 0 0 0-4.142 4.142V9H7v3h2v9.938h3V12h2.021l.592-3H12V6.591A.6.6 0 0 1 12.592 6h.543Z" clip-rule="evenodd"/>
    </svg>  
    </a>
    <a href="https://www.instagram.com/_mrkslp" target="_blank"> 
    <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
      <path fill="white" fill-rule="evenodd" d="M3 8a5 5 0 0 1 5-5h8a5 5 0 0 1 5 5v8a5 5 0 0 1-5 5H8a5 5 0 0 1-5-5V8Zm5-3a3 3 0 0 0-3 3v8a3 3 0 0 0 3 3h8a3 3 0 0 0 3-3V8a3 3 0 0 0-3-3H8Zm7.597 2.214a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2h-.01a1 1 0 0 1-1-1ZM12 9a3 3 0 1 0 0 6 3 3 0 0 0 0-6Zm-5 3a5 5 0 1 1 10 0 5 5 0 0 1-10 0Z" clip-rule="evenodd"/>
    </svg>
    </a>
  </div>
</div>

<!-- Footer -->
<div class="footer">
  Created by Markus with Svelte ✨
</div>
</div>
