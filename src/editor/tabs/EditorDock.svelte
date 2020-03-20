<script>
  import EditorTab from '../tabs/EditorTab.svelte';
  import EditorPannel from '../EditorPannel.svelte';

  // Store the docked panels here.
  let pannels = ["EditorPannel obj ref #1", "EditorPannel obj ref #2"]

  let open_pannel = 0;

  // The tabs order on the dock can be shifted much like other programs.
  function tabDrag(){}

  // Set that tab and pannel to active.
  function tabClick(){}

  // Closes the tab and panel, we also want to warn the user if there are unsaved changes!
  function tabClose(){}

  // Event when the user is moving a tab to another dock.
  // Copy the pannel object to the new dock, remove the pannel and tab here.
  function tabMoveOwnerDock(){}

</script>

<style>
  .dock {
    width: 100%;
    height: 100%;
  }
  h1 {
    text-align: center;
    vertical-align: middle;
    padding: 0px;
    margin: 0px;
  }
</style>

<div class="dock">
  <div class="app_nav">
    {#each pannels as pannel}
      <!-- Replace with pannel.name when the object is linked instead of string. -->
      <EditorTab name={pannel}> </EditorTab>
    {/each}
  </div>
  <h1>DOCK TABS HERE.</h1>
  <slot>
    <!-- This is where we place open_tab.content -->
  </slot>
</div>
