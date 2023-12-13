<script>
  import Counter from "./Counter.svelte";

  let { width, height } = $props(); // instead of `export let`

  const area = $derived(width * height);

  $effect(() => {
    console.log(area);
  });

  let count = $state(0);

  function increment() {
    count += 1;
  }
</script>

<button class="btn btn-xl btn-accent" on:click={increment}>
  clicks: {count}
</button>
