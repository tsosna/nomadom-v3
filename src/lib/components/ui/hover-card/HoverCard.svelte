<script lang="ts" context="module">
	import { getContext, setContext } from 'svelte'
	import type { HoverCard } from '@melt-ui/svelte'

	type HoverCardContest = HoverCard

	function setHoverCardContext(hoverCard: HoverCardContest) {
		setContext('hover-card', hoverCard)
	}

	export function getHoverCardContext(): HoverCardContest {
		return getContext('hover-card')
	}
</script>

<script lang="ts">
	import { createHoverCard, melt } from '@melt-ui/svelte'
	import { Trigger, Content } from '.'

		const hoverCard = createHoverCard({
		openDelay: 350
	})

	setHoverCardContext(hoverCard)

	const {
		elements: { arrow },
		states: { open }
	} = hoverCard
</script>

<slot {Trigger} />
{#if open}
	<slot name='content' {Content} />
	<div use:melt={$arrow} />
{/if}
