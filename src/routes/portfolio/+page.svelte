<script>
    import { onMount } from 'svelte';
    
    let name = "Markus"; // Replace with your name or make dynamic if needed
    let currentPage = ""; // Initialize the current page variable
  
    // Function to set the current page based on the URL
    onMount(() => {
      currentPage = window.location.pathname === '/' ? 'home' : window.location.pathname.substring(1);
    });
  
    // Example portfolio projects
    let projects = [
      {
        title: "E-commerce Project using Angular",
        description: "This is a working e-commerce website with a shopping cart. You can change the amount of items you want to buy. The information is stored in a database. In the shopping cart, you can adjust the quantity of each item or remove items if you want. There’s also an option to select all items at once. You can choose items by clicking the box next to each item.",
        projectImage: "Screenshot 2024-10-10 214428.png" // Image for the project
      },
      {
        title: "Shopping Cart", // Add title for the second image
        description: "This is the shopping cart.", // Add description if needed
        projectImage: "Screenshot 2024-10-10 214440.png" // Second image
      },
    ];
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
        color: white; /* Set default text color to white */
        height: auto; /* Adjust height to auto for better layout */
        overflow: hidden; /* Prevent scrolling */
    }
  
    /* Navbar styles */
    .navbar {
        background-color: black; /* Navbar background color */
        padding: 1rem 0;
        width: 100%; /* Full width */
        display: flex; /* Use flexbox for layout */
        justify-content: space-between; /* Space between logo and links */
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
        color: #ff6347; /* Active color for the current page */
        font-weight: bold; /* Make the active link bold */
    }
  
    /* Portfolio section styles */
    .portfolio-section {
        text-align: center;
        background-color: black; /* Ensure portfolio section has black background */
        padding: 4rem; /* Add padding for spacing */
        width: 100%; /* Full width */
        overflow: hidden; /* Prevent scrolling */
    }
  
    h1 {
        font-size: 2.5rem;
        color: #ff6347;
    }
  
    .project {
        color: #ff6347;
        margin: 2rem 0; /* Margin for spacing between projects */
        padding: 1rem;
        background-color: rgba(255, 99, 71, 0.1); /* Light background for project cards */
        border-radius: 8px; /* Rounded corners */
        display: flex; /* Enable flexbox */
        flex-direction: column; /* Align items vertically */
        align-items: center; /* Center items horizontally */
    }
  
    p {
        font-size: 1.2rem;
        color: white; /* Paragraph color */
        padding: 1.5rem;
    }
  
    img {
        width: 700px; /* Set a fixed width for medium-sized images */
        height: auto; /* Maintain aspect ratio */
        border-radius: 8px; /* Rounded corners for images */
    }
  
    /* Footer styles */
    footer {
        margin-top: auto; /* Push footer to the bottom */
        padding: 1rem; /* Add padding */
        background-color: black; /* Footer background color */
        color: white; /* Footer text color */
        text-align: center; /* Center align text */
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
  
        .portfolio-section {
            padding: 2rem; /* Adjust padding for mobile */
        }
    }
  
    @media (max-width: 480px) {
        .navbar a {
            font-size: 1rem; /* Even smaller font size for extra small screens */
        }
    }
</style>
  
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
  
<!-- Portfolio Section -->
<div class="portfolio-section">
    <h1>My Portfolio</h1>
    {#each projects as project}
        <div class="project">
            <h2>{project.title}</h2>
            <p>{project.description}</p>
            <img src={project.projectImage} alt={project.title} />
        </div>
    {/each}
</div>
  
<!-- Footer -->
<footer>
    Created by {name} with Svelte ✨
</footer>
