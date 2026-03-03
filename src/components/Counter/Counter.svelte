<script lang="ts">
  let { label }: { label: string } = $props();
  let count: number = $state(0);

  let logo: boolean = $state(false);
</script>

<div class={`card ${logo ? 'logo' : 'logo svelte'}`}>
  <h1>{label} : {count}</h1>
  <button class="btn" onclick={() => count++}>Increment</button>
  <button class="btn" onclick={() => (logo = !logo)}>Toggle Logo</button>
</div>

<style>
  .card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    padding: 2rem;
    border-radius: 8px;
    border: 1px solid transparent;
    padding: 1.2em 2.4em;
    background-color: #1a1a1a;
    cursor: pointer;
    transition: border-color 0.25s;
  }

  .btn {
    border-radius: 8px;
    border: 1px solid transparent;
    padding: 0.6em 1.2em;
    font-size: 1em;
    font-weight: 500;
    font-family: inherit;
    background-color: #1a1a1a;
    cursor: pointer;
    transition: border-color 0.25s;
    border-color: #646cff;
    color: #646cff;
    outline: none;

    &:hover {
      color: white;
      background-color: #646cff;
      border-color: white;
    }
  }

  .logo {
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }

  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }

  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
</style>
