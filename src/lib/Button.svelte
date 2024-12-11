<script>
    let {name,count=$bindable()} = $props();
</script>

<button onclick={()=>{count+=1}}>{name}</button>
