<script lang="ts">
	import { i } from '@inlang/sdk-js'
	import { Button } from '$components/ui/button'
	import { cn } from '$lib/utils'
	import { MenuBar } from '$components/ui/menu-bar'

	let className: string | undefined | null = undefined
	export { className as class }
</script>

<div class={cn('flex', className)}>
	<MenuBar>
		<Button href="about" variant="outline" class="border-0 font-manrope font-light tracking-wider">
			{i('navBar.projects')}
		</Button>
		<div slot="item" let:Item>
			<Item />
		</div>
	</MenuBar>
	<Button href="about" variant="outline" class="border-0 font-manrope font-light tracking-wider">
		{i('navBar.about')}
	</Button>
	<Button href="pricing" variant="outline" class="border-0 font-manrope font-light tracking-wider">
		{i('navBar.pricing')}
	</Button>
	<Button href="contact" variant="outline" class="border-0 font-manrope font-light tracking-wider">
		{i('navBar.contact')}
	</Button>
</div>
