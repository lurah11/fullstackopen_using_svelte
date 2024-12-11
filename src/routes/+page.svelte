<script>
  import Button from "$lib/Button.svelte";
  import Stat from "$lib/Stat.svelte";
    let good = $state(0); 
    let neutral = $state(0); 
    let bad = $state(0)
    let all = $state(0)
    let ave = $state(0)
    let pos = $state(0)

    const increaseCount = (counter) => {counter+=1};

</script>

<style>
    table,td,tr,th {
        border:solid 1px blue;
    }
    table {
        margin-top: 20px;
    }
</style>

<h1>EXERCISE 1.6 TO 1.11</h1>

<h1>Give Feedback</h1>

<Button name={"good"}  bind:count={good} />
<Button name={"neutral"}  bind:count={neutral}  />
<Button name={"bad"}  bind:count={bad} />

{#if good>0 || neutral > 0 || bad > 0}
<table>
    <thead>
        <tr>
            <th>Item</th>
            <th>Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>good</td>
            <td>{good}</td>
        </tr>
        <tr>
            <td>neutral</td>
            <td>{neutral}</td>
        </tr>
        <tr>
            <td>bad</td>
            <td>{bad}</td>
        </tr>
        <Stat name={"All"} operation={"all"} {good} {neutral} {bad}/>
        <Stat name={"Average"} operation={"ave"}  {good} {neutral} {bad} />
        <Stat name ={'Positive'} operation={"pos"}  {good} {neutral} {bad} /> 
    </tbody>
</table>

{:else}
<p>No Feedback</p>
{/if}

