<script>
  export let name = 'New Pannel';
</script>

<style>
  .n_pannel {
    padding: 5px;
  }
</style>

<div class="n_pannel">
  <p>{name}</p>
  <slot />
</div>
