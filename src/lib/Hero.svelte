<script>
  import Socials from "./contact/Socials.svelte";
</script>

<section
  id="home"
  class="w-full h-screen flex flex-col md:flex-row justify-center items-center"
>
  <div
    class="flex flex-col justify-center items-center md:items-start text-center md:text-left md:pl-4 md:ml-4 mt-2.5 md:mt-0"
  >
    <div class="text-5xl mt-2.5 md:mt-0">
      <p>
        Full Stack Developer building scalable backends, slick UIs, and
        mentoring devs along the way.
      </p>
      <p>
        — Crafting open-source tools. Obsessed with clean architecture,
        performance, and staying ahead of the tech curve.
      </p>
    </div>
    <div class="text-3xl mt-2.5 md:mt-0 flex flex-col items-start">
      <p class="text-indigo-300 py-2 hover:underline">
        <a href="mailto:rajugowda.towork@gmail.com"
          >rajugowda.towork@gmail.com</a
        >
      </p>
      <span class="text-slate-500 hover:underline"
        ><a target="_blank" href="https://github.com/rajumb0232">GitHub</a
        ></span
      >
      <br />

        <Socials/>
    </div>
  </div>
</section>
