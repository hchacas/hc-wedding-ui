<script>
    let isMenuOpen = false;
    
    function toggleMenu() {
      isMenuOpen = !isMenuOpen;
    }
  </script>
  
  <nav class="container mx-auto px-5 max-w-screen-xl flex items-center justify-between py-4">
    <!-- Logo -->
    <div class="logo text-2xl font-bold text-pink-500">LOVE</div>
  
    <!-- Burger Button for Mobile -->
    <button
      class="md:hidden text-gray-700 focus:outline-none"
      on:click={toggleMenu}
      aria-label="Toggle Menu"
    >
      <!-- Hamburger icon -->
      <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
      </svg>
    </button>
    
    <!-- Mobile Menu -->
    <div class="md:hidden absolute top-16 left-0 right-0 bg-white shadow-md z-10 {isMenuOpen ? '' : 'hidden'}">
      <!-- Mobile menu content -->
      <ul class="py-2 px-4">
        <li class="py-2"><a href="/" class="block">Home</a></li>
        <li class="py-2"><a href="/about" class="block">About</a></li>
        <!-- Add more menu items as needed -->
      </ul>
    </div>
    
    <!-- Desktop Menu - Always visible on larger screens -->
    <div class="hidden md:flex items-center space-x-6">
      <a href="/" class="text-gray-700 hover:text-pink-500">Home</a>
      <a href="/about" class="text-gray-700 hover:text-pink-500">About</a>
      <!-- Add more menu items as needed -->
    </div>
  </nav>