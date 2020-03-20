<script>
  import EditorButton from '../EditorButton.svelte';
  export let name;
  export let exitCall;
</script>

<style>
  .tab {
    padding: 0px;
    display: flex;
    flex-direction: row;
    -webkit-transition: 0.2s;
    transition: 0.2s;
  }
  p{
    padding:4px 12px;
  }
  * {
    margin: 0px;
  }
  .icon{
    fill: aqua;
  }

  .tab:hover {
    background-color: rgba(255, 255, 255, 0.027);
    filter: brightness(1.5);
  }
  .tab:active {
    filter: brightness(0.7);
  }
</style>

<div class="tab">
  <svg class="icon" height="32" width="20">
    <circle cx="16" cy="16" r="4" />
  </svg>
  <p>{name}</p>
  <EditorButton name="X" flat/>
</div>
