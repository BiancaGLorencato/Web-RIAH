<script>
    export let label, id, value, classes;
</script>
    <div class="relative w-full {classes}">
        <label class="block uppercase text-blueGray-600 text-xs font-bold mb-2" for="{id}">{label}</label>
        <input id="{id}" {...$$restProps} class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
        bind:value />     
    </div>
    