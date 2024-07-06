<script>
  const courses = [
    {name: "Git & version control", link: "/learn/git", steps: 64, icon: "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg"},
    {name: "Shell/ Terminal/ Bash", link: "/learn/bash", steps: 64, icon: "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/bash/bash-original.svg"},
    {name: "Docker, images & containers", link: "/learn/docker", steps: 64, icon: "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original-wordmark.svg"},
  ]
  // generates a random course for the `get started` button!
  const courseIndex = Math.floor(Math.random() * courses.length);
</script>

<svelte:head>
<link rel="stylesheet" type='text/css' href="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css" />
  <title>Courses</title>
</svelte:head>

<div class='px-3 sm:px-[20%]'>
  <h1 class='font-extrabold'>What we offer (for now): </h1>
  {#each courses as courses}
    <a href={`${courses.link}`} 
      ><div class='rounded-lg px-12 py-3 hover:bg-slate-200'>
      <img src={courses.icon} alt={`${courses.name} icon`} class="w-6 h-6 inline"/>
      <h3 class='text-black font-bold inline px-3'>{courses.name}</h3>
      </div>
    </a>
  {/each}
  <a class="px-3 my-5 sm:px-[20%]" href={courses[courseIndex].link}>
    <button class='my-5 rounded-lg bg-amber-600 text-black px-6 text-3xl text-center py-4 hover:bg-amber-400 '>Start now (it's fun)</button>
  </a>
</div>
