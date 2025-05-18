<script>
  import Socials from "./contact/Socials.svelte";
  import ShimmerAnimate from "./utils/ShimmerAnimate.svelte";

  // Using Svelte 5's $state for reactive state
  let isAnimated = $state([false, false, false]);

  // Function to run the animation sequence
  function animateSequence() {
    // Reset animations
    isAnimated = [false, false, false];

    // Animate one by one with delays
    setTimeout(() => (isAnimated[0] = true), 0); // First animation starts immediately
    setTimeout(() => {
      isAnimated[0] = false; // End first
      isAnimated[1] = true; // Start second
    }, 3000); // After 3 seconds
    setTimeout(() => {
      isAnimated[1] = false; // End second
      isAnimated[2] = true; // Start third
    }, 6000); // After 6 seconds

    // Restart the sequence after a total duration plus a pause
    // Total animation time is roughly 6s + duration of third animation (assuming it ends before the next trigger)
    // We trigger the next sequence after 11 seconds (6s + ~5s pause)
    setTimeout(() => animateSequence(), 11000);
  }

  // State to ensure the animation sequence only starts once
  let initialized = false;

  // Effect to run on component initialization
  $effect(() => {
    // Prevent running the effect again if state changes after initialization
    if (initialized) return;
    // Mark as initialized
    initialized = true;
    // Start the animation sequence
    animateSequence();
  });
</script>

<section
  id="home"
  class="w-full h-screen flex flex-col md:flex-row justify-center items-center px-4"
>
  <div class="container mx-auto flex flex-col md:flex-row justify-center items-center">
    <div
      class="flex flex-col justify-center items-start text-left md:pl-4 md:ml-4 mt-2.5 md:mt-0"
    >
      <div class="text-3xl sm:text-4xl md:text-5xl mt-2.5 md:mt-0 px-2 sm:px-4 md:px-0">
        <p>
          <span>
            <ShimmerAnimate
              text="Full Stack Developer"
              isAnimated={isAnimated[0]}
              delay={0}
            />
          </span>
          building scalable backends, slick UIs, and
          <span>
            <ShimmerAnimate
              text="mentoring devs"
              isAnimated={isAnimated[1]}
              delay={0}
            />
          </span>
          along the way.
        </p>
        <p> <span>
            <ShimmerAnimate
              text="— Crafting open-source tools"
              isAnimated={isAnimated[2]}
              delay={0}
            />
          </span>
          . Obsessed with clean architecture, performance, and staying ahead of the
          tech curve.
        </p>
      </div>

      <div class="text-xl sm:text-2xl md:text-3xl mt-6 md:mt-10 flex flex-col items-start px-2 sm:px-4 md:px-0">
        <p class="text-indigo-300 py-2 hover:underline">
          <a href="mailto:rajugowda.towork@gmail.com">rajugowda.towork@gmail.com</a>
        </p>
        <span class="text-slate-500 hover:underline">
          <a target="_blank" href="https://github.com/rajumb0232">GitHub</a>
        </span>
        <br />
        <Socials />
      </div>
    </div>
  </div>
</section>