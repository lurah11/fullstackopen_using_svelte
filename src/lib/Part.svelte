<script>
    import Content from '$lib/Content.svelte'
    let {partTitle,contents} = $props(); 
 
</script>

<h3>{partTitle}</h3>

{#if contents.length>0}
    {#each contents as content,i}
    <Content content={content} index={i} />
    {/each}
{/if}