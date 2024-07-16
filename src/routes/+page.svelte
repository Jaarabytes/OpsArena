<script>
  import '../app.css'
  const links = [{name: "Github, ", href: "https://github.com/jaarabytes/ops-arena"},
  {name: "Twitter, ", href: "https://x.com/jaarabytes"},
  {name: "and Status page.", href: "/donate"}]
</script>

<svelte:head>
  <title>OpsArena</title>
</svelte:head>

<main class="flex items-center justify-center h-screen">
  <div class='mx-auto px-3 xl:px-[40%]'>
    <p class='text-3xl my-5 sm:text-[49px] font-extrabold'>Ops-arena</p>
    <p>Learn DevOps, the <b>fun</b> way! </p>
    <button class="text-white border border-slate-700 w-full py-3 my-5 rounded-lg text-xl hover:bg-yellow-900">Login</button>
    <div class="my-5 ">
      {#each links as link}
      <a class="text-white hover:text-yellow-700" href={link.href}>{link.name}</a>
    {/each}
    </div>
  </div>
</main>
