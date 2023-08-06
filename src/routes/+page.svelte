<script lang="ts">
	import { Button } from '$components/ui/button'
	import { i } from '@inlang/sdk-js'

	export let data
	const { projects } = data
</script>

<div>
	<h1>Page</h1>

	{#each projects as { slug }}
		<p>
			{slug}
		</p>
	{/each}

	<Button let:I class="gap-2"><I.Icon let:I><I.Mail /></I.Icon> {i('language')}</Button>
</div>
