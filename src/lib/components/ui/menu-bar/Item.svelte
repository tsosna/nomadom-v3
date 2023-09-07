<script lang="ts">
  import {melt} from '@melt-ui/svelte'
  import {getMenubarContext} from './MenuBar.svelte'
  
  const {builders:{createMenu}} = getMenubarContext()
  const {elements: {item}} = createMenu()
</script>


<div use:melt= {$item}>
  <slot/>
</div>