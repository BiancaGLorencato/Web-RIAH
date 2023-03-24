<script>
  import FooterAdmin from "../Footers/FooterAdmin.svelte";
  import AdminNavbar from "../Navbars/AdminNavbar.svelte";
  import SidebarAdmin from "../Sidebar/SidebarAdmin.svelte";

  export let location;
  export let admin = "";
  export let logo;
</script>
    
<div>
  <SidebarAdmin location={location} />
    <div class="relative md:ml-64 bg-white-100">
      <div class="relative bg-white-500 md:pt-32 pb-32 pt-12">
        <div class="px-4 md:px-10 mx-auto w-full">
          <div>
            <AdminNavbar logo={logo}/>
          </div>
          <div class="mx-auto m-24">
            <slot />
          </div>
        </div>
      </div>
      
      <FooterAdmin />
    </div>
</div>