<script lang="ts">
	import { Theme } from '$components/theme'
	import { Language } from '$components/language'
	import { MenuBar } from '$components/ui/menu-bar'
	import { Button } from '$components/ui/button'
	import { Navbar } from '$components/navbar'

	import { cn } from '$lib/utils'

	let className: string | undefined | null = undefined
	export { className as class }
</script>

<div class={cn('flex justify-between items-center text-accent-foreground bg-accent', className)}>

	<slot  {Theme} {Language} {MenuBar} {Button} {Navbar} />
</div>
