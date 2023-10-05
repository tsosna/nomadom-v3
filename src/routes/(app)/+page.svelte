<script lang="ts">
	import { Navbar } from '$components/navbar'
	export let data
	const { projects } = data
</script>

<Navbar let:Brand let:Menu let:Language let:Theme >
	<Brand />

	<Menu />

	
	<div class="flex">
		<Theme />
		<Language />
	</div>
</Navbar>
