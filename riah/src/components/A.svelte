<script>
   export let href; 
   export let color;
</script>
<div class="relative mb-4">
<a {href} class="text-md mt-10 focus:outline-none {{color}} ">
    <slot />
</a>
</div>