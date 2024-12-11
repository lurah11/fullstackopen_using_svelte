<script>
    let {parts} = $props();
    let total = parts.reduce((acc, cur) => acc + parseInt(cur.exercises), 0);
</script>

<p>Total exercises = {total}</p>