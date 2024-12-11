<script>

import Anecdote from "$lib/Anecdote.svelte"


let raw_index = $state(0); 
</script>

<style>

</style>

<h1>EXERCISE 1.12 TO 1.14</h1>



<Anecdote {raw_index} />


