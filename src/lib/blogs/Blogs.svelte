<script>
  import BlogCard from "./BlogCard.svelte";

  const blogs = [
    {
      title: "How Does Spring Security Authentication Work?",
      description:
        "Understand the authentication system behind Spring Security.",
      imageUrl:
        "https://cdn.hashnode.com/res/hashnode/image/upload/v1743732830768/9c65ffe3-2239-4eb1-9f09-5a6beb631f4d.png?w=1600&h=840&fit=crop&crop=entropy&auto=compress,format&format=webp",
      url: "https://blog.rajugowda.in/how-does-spring-security-authentication-work",
    },
    {
      title: "Key Elements of Spring Security Architecture Explained",
      description:
        "A comprehensive guide to decode each component of the Architecture",
      imageUrl:
        "https://cdn.hashnode.com/res/hashnode/image/upload/v1710865109064/f021fdb9-f48e-4b55-9b05-b83c547fc741.png?w=1600&h=840&fit=crop&crop=entropy&auto=compress,format&format=webp",
      url: "https://blog.rajugowda.in/spring-security-behind-the-curtain",
    },
    {
      title: "SOLID Principles Demystified: A Developer's Roadmap to Clean Code",
      description:
        "A Developer's Guide to Write Elegant and Maintainable Code Using SOLID Principles",
      imageUrl:
        "https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/WtXcbWXK_ww/upload/f2b1eef824a3c3c0694b7c0fd0d1095f.jpeg?w=1600&h=840&fit=crop&crop=entropy&auto=compress,format&format=webp",
      url: "https://blog.rajugowda.in/solid-principles-demystified-a-developers-roadmap-to-clean-code",
    },
  ];
</script>

<section
  class="w-full max-w-screen-lg mx-auto px-4 md:px-6 text-slate-300 flex flex-col items-center mt-10"
>
  <h1 class="text-3xl sm:text-4xl font-bold my-10">Blogs</h1>

  <div class="w-full grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">
    {#each blogs as { title, description, imageUrl, url }}
      <BlogCard {title} {description} {imageUrl} {url} />
    {/each}
  </div>

  <div class="w-full flex justify-center md:justify-end">
    <button
      class="px-8 py-3 bg-blue-600 rounded-xl my-20 hover:bg-blue-700 text-white font-semibold text-lg transition duration-300"
    >
      <a
        target="_blank"
        rel="noopener noreferrer"
        href="https://blog.rajugowda.in">View Blogs →</a
      >
    </button>
  </div>
</section>