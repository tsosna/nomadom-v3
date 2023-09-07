<script lang="ts">
	import { Brand } from './'
	import { cn } from '$lib/utils'

	let className: string | undefined | null = undefined
	export { className as class }

</script>

<nav class=" text-accent-foreground bg-accent">
	<ul class={cn('flex justify-between items-center', className)} >
		<slot {Brand}/>	
	</ul>
</nav>
