<script lang="ts">
  let { label } = $props();
</script>

<button>{label}</button>

<style>
  button {
    display: inline-block;
    border: 1px solid red;
    color: white;
    padding: 8px 16px;
    text-align: center;
    cursor: pointer;
  }
</style>
