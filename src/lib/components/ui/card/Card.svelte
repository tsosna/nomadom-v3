<script lang="ts">
	import { cn } from '$lib/utils'
	import { Header, Title, Description, Content, Footer } from './'
	let className: string | undefined | null = undefined
	export { className as class }
</script>

<div
	class={cn('rounded-lg border bg-card text-card-foreground shadow-sm', className)}
	{...$$restProps}
	on:click
	on:focusin
	on:focusout
	on:mouseenter
	on:mouseleave
>
	<slot {Header} {Title} {Description} {Content} {Footer} />
</div>
