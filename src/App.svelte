<script>
  import Blogs from "./lib/blogs/Blogs.svelte";
  import Explore from "./lib/Explore.svelte";
  import Hero from "./lib/Hero.svelte";
  import Navbar from "./lib/Navbar.svelte";
</script>

<Navbar />

<main class="font-selected px-10 mx-auto max-w-5xl flex flex-col justify-center items-center">
  <Hero />
  <Explore />
</main>
<main class="font-selected flex flex-col justify-center items-center">
  <div class="px-10 mx-auto max-w-5xl w-full">
    <Blogs />
  </div>
</main>

<style>
  :global(html) {
    color: rgb(228, 229, 230);
    height: 100%;
    width: 100%;
    background-color: #060606;
  }
</style>
