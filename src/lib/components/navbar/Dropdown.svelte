<script lang="ts">
  import {LinkPreview} from '$components/ui/link-preview'
  import {Button} from '$components/ui/button'

  export let title: string
  export let dropdown: any
</script>


<LinkPreview let:Trigger>
  <Trigger>
    <Button variant="outline" class="gap-2" >{title}</Button>
  </Trigger>

  <div slot="content" let:Content>
    <Content class='flex flex-col gap-2 '>
      
      
      <slot name='dropdown'/>
    </Content>
  </div>
</LinkPreview>