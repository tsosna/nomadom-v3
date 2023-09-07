<script lang="ts">
	import { getLinkPreviewContext } from './LinkPreview.svelte'
	import { melt } from '@melt-ui/svelte'

	import { cn } from '$lib/utils'

	let className: string | undefined | null = undefined
	export { className as class }

	const {
		elements: { content }
	} = getLinkPreviewContext()
</script>

<div
	use:melt={$content}
	class={cn(
		'z-50 max-w-min rounded-md border bg-popover p-4 text-popover-foreground shadow-md outline-none animate-in zoom-in-90 mt-1',
		className
	)}
	{...$$restProps}
>
	<slot />
</div>
