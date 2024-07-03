<script>
  import '../app.css'
  
  // add donations as soon as possible
  const builders = [{name: "Jaarabytes", link: "jaarabytes"}]
</script>

<div class='my-5 px-3 sm:px-[20%]'>
  <p class='text-3xl sm:text-[49px] font-extrabold'>Learn DevOps, the fun way! </p>
    <div class='my-5'>
      <p class=''>Unfortunately we are still in development. </p>
      <p>We however accept all contributions (ideas, code itself and donations) </p>
      <p class='mt-5'>Builders: </p>
      {#each builders as builder}
        <li><a href={`https://x.com/${builder.link}`}>{builder.name}</a></li>
      {/each}
      <p class="my-5">You can contact us through X (formerly twitter) DM's. </p>
      <p class=''>For code contributions: </p>
      <a href="https://github.com/Jaarabytes/OpsArena">https://github.com/Jaarabytes/OpsArena</a>
      <p class='my-3'>Issues: </p>
      <a href="https://github.com/Jaarabytes/OpsArena/issues/new">https://github.com/Jaarabytes/OpsArena/issues/new</a>
      <p class='my-3'>To donate: </p>
      <a href='/donate'>Click me!</a>
    </div>
</div>
