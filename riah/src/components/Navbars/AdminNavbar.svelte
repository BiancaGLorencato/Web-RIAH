<script>
import UserDropdown from "../Dropdowns/UserDropdown.svelte";


  // core components
  export let logo;

</script>

<!-- Navbar -->
<nav
  class="absolute top-0 left-0 w-full z-10 bg-transparent md:flex-row md:flex-nowrap md:justify-start flex items-center p-4"
>
  <div
    class="w-full mx-autp items-center flex justify-between md:flex-nowrap flex-wrap md:px-10 px-4"
  >
    <!-- Brand -->
    <div
      class="text-white text-sm hidden lg:inline-block">
      <img src={logo} alt="logo"  class="h-20 w-30 object-center">
    </div>
    
    <!-- User -->
    <ul class="flex-col md:flex-row list-none items-center hidden md:flex">
      <UserDropdown />
    </ul>
  </div>
</nav>
<!-- End Navbar -->
