<script>
  import { count } from './stores'

  const reset = () => {
    // $count = 0
    // or
    count.set(0)
  }
</script>

<button on:click={reset}>Reset Count</button>
