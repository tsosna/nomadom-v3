<script lang="ts" context="module">
	import type { Menubar } from '@melt-ui/svelte'
	import { getContext, setContext } from 'svelte'

	type MenubarContext = Menubar

	function setMenubarContext(Menubar: MenubarContext) {
		setContext('menubar', Menubar)
	}

	export function getMenubarContext(): MenubarContext {
		return getContext('menubar')
	}
</script>

<script lang="ts">
	import { createMenubar, melt } from '@melt-ui/svelte'
	import { Item } from '.'
	
	const {
		elements: { menubar },
		builders: { createMenu }
	} = createMenubar()
	const {
		elements: { trigger, menu },
		states: { open }
	} = createMenu()

	setMenubarContext(createMenubar())
</script>


<div use:melt={$menubar}>
	<button use:melt={$trigger}>
		<slot />
	</button>
	<div use:melt={$menu}>
		<slot name="item" {Item} />
	</div>
</div>


