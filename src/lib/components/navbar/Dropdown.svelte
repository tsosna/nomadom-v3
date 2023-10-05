<script lang="ts">
	import { i } from '@inlang/sdk-js'
	import { Button } from '$components/ui/button'

	export let currentItem: number = 0
	export let item: {
		icon: string | null
		name: string
		slug: string
		path: string
		currentItem: number
	}

	item.icon = null

</script>

<Button
	let:Icon
	href={`${item.path}/${item.slug}`}
	variant="outline"
	class="gap-2 border-0"
	aria-label={item.name}
	on:mouseenter={() => (currentItem = item.currentItem)}
>
	<svelte:component this={Icon[item.icon]} aria-label={i(item.name)} {...$$props} />
	<span class="text-lg font-light font-manrope">
		{item.name}
	</span>
</Button>
