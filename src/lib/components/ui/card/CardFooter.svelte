<script lang="ts">
	import { cn } from "$lib/utils";

	let className: string | undefined | null = undefined;
	export { className as class };
</script>

<div class={cn("flex items-center p-6 pt-6", className)} {...$$restProps}>
	<slot />
</div>
