<script>
    export let label, id, value, classes, info;
</script>
     
        <label class="inline-flex items-center cursor-pointer ml-4 " for="{id}">
            <input id="{id}" {...$$restProps} class="border-0 px-3 py-3"
            bind:value /> <span class="ml-2 text-sm"> {info} </span></label>    
    