<script>
  import { page } from '$app/stores'
  import { onMount } from 'svelte'
  import '../app.css'

  let catImage = '';
  
  // okay, this is exactly useEffect
  onMount(() => {
    if ( $page.status === 404 || $page.status === 500 || $page.status === 403 || $page.status === 401 ) {
      // showcase a cat image for each http status error! Hell yeah
      catImage = `https://http.cat./${$page.status}.jpg`
    }
  })
</script>

<svelte:head>
  <title>{$page.status}: {$page.error?.message}</title>
</svelte:head>

<main>
  {#if catImage }
    <a href="/"><img src={catImage} class='mx-auto' alt="HTTP status cat!" /></a>
  {:else}
    <p class='text-center my-5'>An error occured. Please go <a href="/">HOME</a></p>
  {/if}
</main>
