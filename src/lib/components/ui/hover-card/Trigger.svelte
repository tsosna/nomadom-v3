<script lang="ts">
  import { getHoverCardContext} from './HoverCard.svelte'
  import {melt} from '@melt-ui/svelte'

  import {Button} from '$components/ui/button'

  const {elements: {trigger}} = getHoverCardContext()

</script>

<button use:melt={$trigger}>
  <slot {Button}/>
</button>