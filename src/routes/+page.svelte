<script>
  import { onMount } from 'svelte';

  let name = "Markus"; // Replace with your name or make dynamic if needed
  let currentPage = ""; // Initialize the current page variable

  // Function to set the current page based on the URL
  onMount(() => {
    currentPage = window.location.pathname === '/' ? 'home' : window.location.pathname.substring(1);
  });
</script>

<style>
  /* Overall body style for alignment */
  body {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0; /* Remove default margin */
    font-family: Arial, sans-serif; /* Added a default font */
    background-color: black; /* Set the background color to black */
    height: 100vh; /* Make sure it covers full height */
    justify-content: space-between; /* Space out content */
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
    padding: 16.2rem; /* Add padding for spacing */
  }

  h1 {
    font-size: 2.5rem;
    color: white; /* Heading color */
  }

  p {
    font-size: 1.2rem;
    color: white; /* Default paragraph color */
  }

  /* Change paragraph color to blue if on the portfolio page */
  .portfolio-page p {
    color: blue; /* Set paragraph color to blue */
  }

  /* Footer styles */
  .footer {
    text-align: center; /* Center text in footer */
    padding: 1rem 0; /* Add padding */
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
<section class="welcome-section {currentPage === 'portfolio' ? 'portfolio-page' : ''}">
  <h1>Hello! 👋🏼</h1>
  <h1>I'm Markus Alop</h1>
  <h1>A Student 🧑🏽‍💻 in Gordon College</h1>
</section>

<!-- Footer Section -->
<footer class="footer">
  Created by Markus Alop with Svelte ✨
</footer>
</div>