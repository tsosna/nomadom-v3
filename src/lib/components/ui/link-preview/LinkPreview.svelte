<script lang="ts" context="module">
	import { getContext, setContext } from 'svelte'
	import type { LinkPreview } from '@melt-ui/svelte'

	type LinkPreviewContest = LinkPreview

	function setLinkPreviewContext(LinkPreview: LinkPreviewContest) {
		setContext('link-preview', LinkPreview)
	}

	export function getLinkPreviewContext(): LinkPreviewContest {
		return getContext('link-preview')
	}
</script>

<script lang="ts">
	// import type { CreateLinkPreviewProps } from '@melt-ui/svelte'
	import { createLinkPreview, melt } from '@melt-ui/svelte'
	import { Trigger, Content } from '.'

	const LinkPreview = createLinkPreview({
		openDelay: 350
	})

	setLinkPreviewContext(LinkPreview)

	const {
		elements: { arrow },
		states: { open }
	} = LinkPreview

	// export let openDelay: CreateLinkPreviewProps['openDelay'] = 350
</script>

<slot {Trigger} />
{#if $open}
	<slot name="content" {Content} />
	<div use:melt={$arrow} />
{/if}
