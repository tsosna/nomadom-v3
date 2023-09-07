<script lang="ts">
	import { i } from '@inlang/sdk-js'
	import { Button } from '$components/ui/button'
	import { LinkPreview } from '$components/ui/link-preview/index.js'
	import { Header } from '$components/header'
	export let data
	const { projects } = data
</script>

<Header let:Theme let:Language let:Navbar>
	<Navbar let:Brand>
		<Brand />
	</Navbar>

	<div class="flex">
		<Theme />
		<Language />
	</div>
</Header>
