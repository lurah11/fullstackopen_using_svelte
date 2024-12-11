<script>
    let {parts} = $props();
</script>

{#if parts.length > 0}
<ul>
    {#each parts as part,i}
    <li>
        {i}. {part.name} ({part.exercises} exercises)
    </li>
    {/each}
</ul>
{:else}
<p>No Info Available</p>
{/if}