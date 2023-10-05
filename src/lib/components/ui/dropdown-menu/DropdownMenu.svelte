<script lang="ts" context="module">
	import { getContext, setContext } from 'svelte'
	import type { DropdownMenu } from '@melt-ui/svelte'

	type DropdownMenuContest = DropdownMenu

	function setDropdownMenuContext(DropdownMenu: DropdownMenuContest) {
		setContext('dropdown-menu', DropdownMenu)
	}

	export function getDropdownMenuContext(): DropdownMenuContest {
		return getContext('dropdown-menu')
	}
</script>

<script lang="ts">
  import { createDropdownMenu, melt } from '@melt-ui/svelte'

  const DropdownMenu = createDropdownMenu({})
setDropdownMenuContext(DropdownMenu)

  const { elements: { arrow }, states: { open } } = DropdownMenu


  
</script>



<slot {Trigger} />
{#if $open}
  <slot name="menu" {Menu} >
    <slot name="item" {Item} />
  <slot/>
  <div use:melt={$arrow} />
{/if}