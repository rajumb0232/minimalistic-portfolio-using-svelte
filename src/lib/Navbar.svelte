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
</script>

<nav
  class="fixed w-screen p-6 px-10 flex justify-center items-center font-bold font-selected text-xl"
>
  <span>👋 Hi, I'm Raju</span>
  <ul class="flex justify-center items-center ml-auto">

    {#each links as link}

      <li class="px-4 hover:underline">
        <a href={link.href}>{link.name}</a>
      </li>

    {/each}

  </ul>
</nav>
