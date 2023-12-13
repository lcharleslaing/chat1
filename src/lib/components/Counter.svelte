<script>
  import RunesCounter from "./RunesCounter.svelte";

  let count = 0;

  function increment() {
    count += 1;
  }
</script>

<button class="btn btn-xl btn-primary m-4" on:click={increment}>
  clicks: {count}
</button>
<RunesCounter />
<RunesCounter />
