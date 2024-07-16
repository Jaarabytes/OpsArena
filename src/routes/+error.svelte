<script>
  import { page } from '$app/stores'
  import { onMount } from 'svelte'
  import '../app.css'


  let catImage = '';
  
  // okay, this is exactly useEffect
  onMount(() => {
    if ( $page.status === 404 || $page.status === 500 ) {
      // only for 404, 500 and 401 maybe
      catImage = `https://http.cat./${$page.status}.jpg`
    }
  })
</script>

<svelte:head>
  <title>{$page.status}: {$page.error?.message}</title>
</svelte:head>

<main>
  {#if catImage }
    <a href="/"><img src={catImage} class='mx-auto' alt="HTTP status dog!" /></a>
  {:else}
    <p class='text-center my-5'>An error occured. Please go <a href="/">HOME</a></p>
  {/if}
</main>
