<script lang="ts">
	import { Brand, Menu, Dropdown } from './'
	import { Theme } from '$components/theme'
	import { Language } from '$components/language'
	import { cn } from '$lib/utils'

	let className: string | undefined | null = undefined
	export { className as class }
</script>

<nav class={cn('flex justify-between items-center text-accent-foreground bg-accent', className)}>
	<slot {Brand} {Menu} {Theme} {Language} {Dropdown}/>
</nav>
