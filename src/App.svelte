<script>
  //   import { onDestroy } from 'svelte'
  import { count } from './stores'
  import Button from './Button.svelte'
  import Resetter from './Resetter.svelte'
  export let name

  //   const unsubscribe = count.subscribe((value) => {
  //     console.log(value)
  //   })

  const increment = () => {
    count.update((n) => n + 1)
    // or
    // $count += 1
  }

  //   onDestroy(() => unsubscribe())
</script>

<main>
  <h1>Hi {name}!{$count}</h1>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
  <form>
    <input type="text" bind:value={name} />
  </form>
  <Button count={$count} handelClick={increment} />
  <Resetter />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
