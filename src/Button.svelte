<script>
  export let count = 42
  export let handelClick = () => {
    count += 1
  }
</script>

<button on:click={handelClick}>count: {count}</button>

<style>
</style>
