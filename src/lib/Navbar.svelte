<script>
  const links = [
    {
      name: "Home",
      href: "#home",
    },
    {
      name: "Explore",
      href: "#explore",
    },
    {
      name: "Contact",
      href: "#contact",
    },
  ];

  // State to control the visibility of the mobile menu
  let isMobileMenuOpen = false;

  // Function to toggle the mobile menu state
  function toggleMobileMenu() {
    isMobileMenuOpen = !isMobileMenuOpen;
  }

  // Function to close the mobile menu (useful when a link is clicked)
  function closeMobileMenu() {
    isMobileMenuOpen = false;
  }
</script>

<nav
  class="fixed z-40 w-screen pt-6 px-4 md:px-10 bg-inherit/95 backdrop-blur"
>
  <div class="container mx-auto flex justify-between items-center font-bold font-selected text-xl">
    <span>👋 Hi, I'm Raju</span>

    <button class="md:hidden block p-2 focus:outline-none" on:click={toggleMobileMenu}>
      <svg
        class="w-6 h-6 text-current"
        fill="none"
        stroke="currentColor"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg"
      >
        {#if isMobileMenuOpen}
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M6 18L18 6M6 6l12 12"
          ></path>
        {:else}
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          ></path>
        {/if}
      </svg>
    </button>

    <ul class="hidden md:flex justify-center items-center ml-auto">
      {#each links as link}
        <li class="px-4 hover:underline">
          <a href={link.href}>{link.name}</a>
        </li>
      {/each}
    </ul>
  </div>

  {#if isMobileMenuOpen}
    <ul
      class="md:hidden flex flex-col items-center bg-inherit/95 backdrop-blur w-full py-4 mt-4 space-y-4 border-t border-gray-700"
    >
      {#each links as link}
        <li class="hover:underline">
          <a href={link.href} on:click={closeMobileMenu}>{link.name}</a>
        </li>
      {/each}
    </ul>
  {/if}
</nav>