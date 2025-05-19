<script>
  import Blogs from "./lib/blogs/Blogs.svelte";
  import Contact from "./lib/contact/Contact.svelte";
  import Explore from "./lib/Explore.svelte";
  import Footer from "./lib/footer/footer.svelte";
  import Hero from "./lib/Hero.svelte";
  import Navbar from "./lib/Navbar.svelte";
  import Testimonials from "./lib/testimonials/Testimonials.svelte";
</script>

<Navbar />

<main class="font-selected w-full">
  <div class="max-w-5xl mx-auto px-4 md:px-6 lg:px-8">
    <Hero />
    <Explore />
    <Blogs />
    <Testimonials />
    <Contact />
  </div>
</main>

<Footer />

<style>
  :global(html) {
    color: rgb(228, 229, 230);
    height: 100%;
    width: 100%;
    background-color: #060606;
  }
</style>