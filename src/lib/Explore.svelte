<script>
  import Aboutme from "./explore/Aboutme.svelte";
  import Skills from "./explore/Skills.svelte";
  import Projects from "./explore/Projects.svelte";
</script>

<section
  id="explore"
  class="w-full min-h-screen max-w-screen-lg mx-auto md:py-20 px-0 flex flex-col items-start md:px-10 md:grid md:grid-cols-2 md:grid-rows-2 md:gap-8"
>
  <div
    class="cursor-pointer p-5 rounded-4xl hover:bg-green-500/20 hover:border-2 hover:border-green-400 hover:shadow-[0_0_60px] hover:shadow-green-500/20 transition-all duration-300 flex flex-col w-full mb-8 md:mb-0 md:col-start-1 md:row-span-2"
  >
    <h2 class="text-3xl font-bold mb-4">About Me</h2>
    <p class="text-lg text-gray-200">
      I'm a Full Stack Developer and Mentor with 3+ years in tech and 2+ years
      of hands-on industry experience. Majorly focussed on backend development
      with Spring Boot, where I specialize in building scalable microservices.
    </p> <br>
    <p class="text-lg text-gray-200">
      Frontend? Not a stranger. I’ve built production-ready UIs using React,
      TailwindCSS, React Router, and Redux.
    </p>
    <Aboutme />
  </div>

  <div
    class="cursor-pointer p-5 rounded-4xl hover:bg-purple-400/20 hover:border-2 hover:border-purple-300 hover:shadow-[0_0_60px] hover:shadow-purple-400/20 transition-all duration-300 w-full mb-8 md:mb-0 md:col-start-2 md:row-start-1"
  >
    <h2 class="text-3xl font-bold mb-4">Skills</h2>
    <div class="flex flex-wrap gap-2">
      {#each ["java_8", "java_script", "react_js", "spring_framework", "spring_boot", "rest_apis", "microservices", "my_sql", "mongodb", "go_lang", "svelte"] as skill}
        <span class="bg-white/20 px-3 py-1 rounded-lg text-lg">{"#" + skill}</span>
      {/each}
    </div>

    <Skills />
  </div>

  <div
    class="cursor-pointer p-4 hover:p-5 rounded-4xl hover:bg-blue-400/20 border-2 border-white/10 hover:border-blue-300 hover:shadow-[0_0_60px] hover:shadow-blue-400/20 transition-all duration-300 w-full md:col-start-2 md:row-start-2"
  >
    <h2 class="text-3xl font-bold mb-4">Projects</h2>
    <p class="text-lg text-gray-200">Click to view projects.</p>
    <Projects />
  </div>
</section>
