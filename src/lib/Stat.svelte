<script>
    let {name,operation,good,neutral,bad} = $props();

    let all = $derived.by(() => good + neutral * 0 + bad * (-1));
    let totalVote = $derived.by(() => good + neutral + bad);
    let average = $derived.by(() => totalVote ? all / totalVote : 0);
    let positive = $derived.by(() => totalVote ? (good / totalVote) * 100 : 0);

</script>

<style>
    table,td,tr,th {
        border:solid 1px blue;
    }
</style>

{#if operation=='all'}
    <tr>
        <td>{name}</td>
        <td>{all}</td>
    </tr>
{:else if operation=='ave'}
    <tr>
        <td>{name}</td>
        <td>{average.toFixed(2)}</td>
    </tr>
{:else}
<tr>
    <td>{name}</td>
    <td>{positive.toFixed(2)}</td>
</tr>
{/if}