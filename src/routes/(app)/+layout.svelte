<script lang="ts">
	// import '../app.postcss'
	import { i } from '@inlang/sdk-js'
</script>


<h1>App layout</h1>

<slot />

<svelte:head>
  <link rel="icon" href="favicon.png" />  
  <title>Dashboard</title>
  <meta name="description" content="Dashboard" />
</svelte:head>