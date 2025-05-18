<script>
  import LinkedInSvg from "./svgs/LinkedIn_svg.svelte";
</script>

<div
  id="home"
  class="w-full h-screen flex flex-col md:flex-row justify-center items-center"
>
  <!-- <div>
    <img
      src="https://avatars.githubusercontent.com/u/112748321?v=4"
      alt="Raju's Avatar"
      class="rounded-full max-w-36 max-h-36 mb-4"
    />
  </div> -->
  <div
    class="flex flex-col justify-center items-center md:items-start text-center md:text-left md:pl-4 md:ml-4 mt-2.5 md:mt-0"
  >
    <!-- <h1 class="text-5xl">👋 Hi, I'm Raju</h1> -->
    <div class="text-5xl pl-4 mt-2.5 md:mt-0">
      <p>
        Full Stack Developer building scalable backends, slick UIs, and
        mentoring devs along the way.
      </p>
      <p>
        — Crafting open-source tools. Obsessed with clean architecture,
        performance, and staying ahead of the tech curve.
      </p>
    </div>
    <div class="text-3xl pl-4 mt-2.5 md:mt-0">
      <p class="text-indigo-300 py-2">rajugowda.towork@gmail.com</p>
      <span class="my-2 p-0 text-slate-500">GitHub</span>
      <br />
      <div class="py-2 w-6 h-6">
        <LinkedInSvg />
      </div>
    </div>
  </div>
</div>
