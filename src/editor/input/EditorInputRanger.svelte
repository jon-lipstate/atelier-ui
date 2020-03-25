<script>
  export let val_min = 0;
  export let val_max = 10;

  export let onclick;
  export let updateEvent;
</script>

<style>
  input {
    display: block;
    background-color: #ffffff;
    border-radius: 5px;
    -webkit-box-shadow: rgba(0, 0, 0, 0.23) 0px 3px 8px;
    box-shadow: rgba(0, 0, 0, 0.23) 0px 3px 8px;
    -webkit-transition: 0.5s;
    transition: 0.5s;
    -webkit-transition: 0.2s;
    margin: 4px;
  }

  input:hover {
    -webkit-box-shadow: rgba(0, 0, 0, 0.416) 0px 3px 9px;
    box-shadow: rgba(0, 0, 0, 0.416) 0px 3px 9px;
  }
  input:active {
    background-color: #faf5ff;
  }
</style>

<input type="number" min={val_min} max={val_max} on:click={onclick()} on:update={updateEvent()} />
