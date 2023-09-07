<script lang="ts">
  import { getLinkPreviewContext} from './LinkPreview.svelte'
  import {melt} from '@melt-ui/svelte'
  
  const {elements: {trigger}} = getLinkPreviewContext()

</script>


<div use:melt={$trigger} >
  <slot/>
</div>

<!-- 
  how to use:melt in the svelte component
 -->
