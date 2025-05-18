<script>
  import Socials from "./contact/Socials.svelte";
  import ShimmerAnimate from "./utils/ShimmerAnimate.svelte";

  let isAnimated = $state([false, false, false]);

  function animateSequence() {
    isAnimated = [false, false, false];

    // Animate one by one
    setTimeout(() => (isAnimated[0] = true), 0);
    setTimeout(() => {
      isAnimated[0] = false;
      isAnimated[1] = true;
    }, 3000);
    setTimeout(() => {
      isAnimated[1] = false;
      isAnimated[2] = true;
    }, 6000);

    // Restart after 5s pause once all are done
    setTimeout(() => animateSequence(), 11000);
  }

  let initialized = false;

  $effect(() => {
    if (initialized) return;
    initialized = true;
    animateSequence();
  });
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
        <span
          ><ShimmerAnimate
            text="Full Stack Developer"
            isAnimated={isAnimated[0]}
            delay={0}
          /></span
        >
        building scalable backends, slick UIs, and
        <span
          ><ShimmerAnimate
            text="mentoring devs"
            isAnimated={isAnimated[1]}
            delay={0}
          /></span
        >
        along the way.
      </p>
      <p>
        <span
          ><ShimmerAnimate
            text="— Crafting open-source tools"
            isAnimated={isAnimated[2]}
            delay={0}
          /></span
        >
        . Obsessed with clean architecture, performance, and staying ahead of the
        tech curve.
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

      <Socials />
    </div>
  </div>
</section>
