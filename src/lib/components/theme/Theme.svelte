<script lang="ts">
	import { i } from '@inlang/sdk-js'
	import { Sun, Moon } from 'lucide-svelte'
	import { Button } from '$components/ui/button'
	import { toggleTheme, theme } from '$lib/theme'
	import {LinkPreview} from '$components/ui/link-preview'

	const I = { Sun, Moon }

	const themes = ['Sun', 'Moon']
</script>

<LinkPreview let:Trigger> 
	<Trigger>
		<Button variant="outline" aria-label={i('theme.phrase')}>
			<svelte:component this={I[$theme]} aria-label={i('theme.phrase')} />
		</Button>
	</Trigger>
	<div slot="content" let:Content>
		<Content class="flex flex-col gap-2">
			{#each themes as item}
				<Button
					on:click={() => toggleTheme(item)}
					variant={$theme === `${item}` ? 'disabled' : 'outline'}
					class="gap-2"
					aria-label={i(`theme.theme${item}`)}
				>
					<svelte:component this={I[item]} aria-label={i(`theme.theme${item}`)} />
					{i(`theme.theme${item}`)}
				</Button>
			{/each}
		</Content>
	</div>
</LinkPreview>
