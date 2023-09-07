<script lang="ts">
	import { i, languages, switchLanguage } from '@inlang/sdk-js'
	import { Button } from '$components/ui/button'
	import {LinkPreview} from '$components/ui/link-preview'
</script>

<LinkPreview let:Trigger>
	<Trigger>
		<Button let:Icon variant="outline" class="gap-2"><Icon let:Globe><Globe /></Icon> {i(`language`)}</Button>
	</Trigger>

	<div slot="content" let:Content>
		<Content class='flex flex-col gap-2 '>
			{#each languages as lang}
				<Button variant="outline"  on:click={() => switchLanguage(lang)} aria-label={i(`language.${lang}`)}>
					{i(`language.${lang}`)}
				</Button>
			{/each}
		</Content>
	</div>
</LinkPreview>
