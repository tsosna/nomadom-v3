<script lang="ts">
  import { getHoverCardContext} from './HoverCard.svelte'
  import {melt} from '@melt-ui/svelte'

  const {elements: {content,arrow}} = getHoverCardContext()

</script>

<div use:melt={$content}>
  <slot />
</div>