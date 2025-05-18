<script>
  import hashnodeIcon from "../../public/socials/hashnode-icon.svg";
  import linkedInIcon from "../../public/socials/linkedin-icon.svg";
  import blogIcon from "../../public/socials/blog-icon.svg";
  const socials = [
    {
      name: "LinkedIn",
      url: "https://www.linkedin.com/in/raju-gowda-dev",
      icon: linkedInIcon,
    },
    {
      name: "Hashnode",
      url: "https://hashnode.com/@RajuGowda",
      icon: hashnodeIcon,
    },
    {
      name: "blogs",
      url: "https://blog.rajugowda.in",
      icon: blogIcon,
    },
  ];
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

      <div class="flex justify-center items-center bg-none">
        {#each socials as { url, icon }}
          <div
            class="mr-6 w-7 h-7 bg-transparent rounded-sm hover:shadow-[0_0_20px_rgb(98,116,142)] transition-all duration-150"
          >
            <a href={url} target="_blank" rel="noopener noreferrer">
              <img
                src={icon}
                alt="Social Icon"
                class="w-full h-full rounded-sm"
              />
            </a>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>
