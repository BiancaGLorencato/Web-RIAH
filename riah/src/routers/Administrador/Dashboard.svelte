<script>
import AdminMenu from "../../components/Headers/AdminMenu.svelte";

      export let location;
      export let admin = "";
      export let logo;

      logo = sessionStorage.logo;
</script>
<AdminMenu logo={logo}></AdminMenu>