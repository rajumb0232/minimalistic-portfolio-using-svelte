<script>
  import hashnodeIcon from "../../../public/socials/hashnode-icon.svg";
  import linkedInIcon from "../../../public/socials/linkedin-icon.svg";
  import blogIcon from "../../../public/socials/blog-icon.svg";
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

<div class="flex justify-center items-center bg-none">
  {#each socials as { url, icon }}
    <div
      class="mr-6 w-7 h-7 bg-transparent rounded-sm hover:shadow-[0_0_20px_rgb(98,116,142)] transition-all duration-150"
    >
      <a href={url} target="_blank" rel="noopener noreferrer">
        <img src={icon} alt="Social Icon" class="w-full h-full rounded-sm" />
      </a>
    </div>
  {/each}
</div>
