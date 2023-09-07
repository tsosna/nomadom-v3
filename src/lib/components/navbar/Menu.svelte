<script lang="ts">
	import { i } from "@inlang/sdk-js"
	import { Button } from "$components/ui/button"
	import {LinkPreview} from "$components/ui/link-preview"
 
</script>






<Button href="about" variant="outline" class="border-0 font-manrope font-light tracking-wider">
	{i('navBar.about')}
</Button>
<Button href="pricing" variant="outline" class="border-0 font-manrope font-light tracking-wider">
	{i('navBar.pricing')}
</Button>
<Button href="contact" variant="outline" class="border-0 font-manrope font-light tracking-wider">
	{i('navBar.contact')}
</Button>