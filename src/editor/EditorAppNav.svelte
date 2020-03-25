<script>
	import EditorButton from './EditorButton.svelte';

	export let entrys;

	function os_trigger_min(){}
	function os_trigger_resize(){}
	function os_trigger_exit(){}
</script>

<style>
  .app_nav {
    box-shadow: none;
  }

  .windowButton{
		display: flex;
		flex: row;
		position: fixed;
		top: 0;
		right: 0;
		z-index: 10;
	}

	.os_button{
		padding: 10px;
		height: 20px;
		width: 36px;
		transition: 0.5s;
		cursor: pointer;
	}

	.os_button:hover{
		background-color: #0f50c0;
	}

	.nav_buttons{
		top: -1px;
	}

  .icon{
		padding: 0px 10px;
	}
</style>

<div class="app_nav">

  {#each entrys as item}
    <EditorButton flat name={item.lable} />
  {/each}

	<div class="windowButton">
		<div on:click={os_trigger_min} class="os_button">
			<img class="icon" src="svg/os_min.svg" alt="">
		</div>

		<div on:click={os_trigger_resize} class="os_button">
			<img class="icon" src="svg/os_resize.svg" alt="">	
		</div>

		<div on:click={os_trigger_exit} class="os_button">
			<img class="icon" src="public/svg/os_exit.svg" alt="">
		</div>
	</div>

</div>
