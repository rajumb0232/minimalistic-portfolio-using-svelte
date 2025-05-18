<script>
  import Aboutme from "./explore/Aboutme.svelte";
  import Skills from "./explore/Skills.svelte";
  import Projects from "./explore/Projects.svelte";
</script>

<section
  id="explore"
  class="h-screen w-3xl grid grid-cols-2 grid-rows-2 gap-8 p-10"
>
  <!-- About Me -->
  <div
    class="cursor-pointer col-start-1 p-5 row-span-2 rounded-4xl hover:bg-green-500/20 hover:border-2 hover:border-green-400 hover:shadow-[0_0_60px] hover:shadow-green-500/20 transition-all duration-300 flex flex-col"
  >
    <h2 class="text-3xl font-bold">About Me</h2>
    <p>
      I'm a Full Stack Developer and Mentor with 3+ years in tech and 2+ years
      of hands-on industry experience. My core strength lies in backend
      development with Spring Boot, where I specialize in building scalable
      microservices
    </p>
    <Aboutme />
  </div>

  <!-- Skills -->
  <div
    class="cursor-pointer col-start-2 row-start-1 p-5 rounded-4xl hover:bg-purple-400/20 hover:border-2 hover:border-purple-300 hover:shadow-[0_0_60px] hover:shadow-purple-400/20 transition-all duration-300"
  >
    <h2 class="text-3xl font-bold mb-4">Skills</h2>
    <div class="flex flex-wrap gap-2">
      {#each ["java_8", "java_script", "react_js", "spring_framework", "spring_boot", "rest_apis", "microservices", "my_sql", "mongodb", "go_lang", "svelte"] as skill}
        <span class="bg-white/20 px-3 py-1 rounded-lg">{"#" + skill}</span>
      {/each}
    </div>

    <Skills />
  </div>

  <!-- Projects -->
  <div
    class="cursor-pointer col-start-2 row-start-2 p-4 hover:p-5 rounded-4xl hover:bg-blue-400/20 border-2 border-white/10 hover:border-blue-300 hover:shadow-[0_0_60px] hover:shadow-blue-400/20 transition-all duration-300"
  >
    <h2 class="text-3xl font-bold">Projects</h2>
    <p>Click to view projects.</p>
    <Projects />
  </div>
</section>
