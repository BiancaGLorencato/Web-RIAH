<script>
import AdminMenu from "../../../components/Headers/AdminMenu.svelte";


    export let logo;
    logo = sessionStorage.logo;

   let  titule = "Urgências cadastradas";
   let headers = ['Nome', 'Informações', 'status', ' '];
</script>

<AdminMenu logo={logo}>
    <div
  class="relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded"
>
  <div class="rounded-t mb-0 px-4 py-3 border-0">
    <div class="flex flex-wrap items-center">
      <div class="relative w-full px-4 max-w-full flex-grow flex-1">
        <h3 class="font-semibold text-base text-blueGray-700">
          {titule} 
        </h3>
      </div>
      <a href="/#/admin/urgencia/novo"
      class="bg-indigo-500 text-white active:bg-indigo-600 text-xs font-bold uppercase px-3 py-1 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150"
      type="button"
    >
      Novo
    </a>
    </div>
  </div>
  <div class="block w-full overflow-x-auto">
    <!-- Projects table -->
    <table class="items-center w-full bg-transparent border-collapse">
      <thead>
        <tr>
         {#each headers as header}
          <th
            class="px-6 bg-blueGray-50 text-blueGray-500 align-middle border border-solid border-blueGray-100 py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left"
          >
            {header}
          </th>
          {/each}
        </tr>
      </thead>
      <tbody>
        <tr>
          <th class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4 text-left"
          >
            Triagem
          </th>
          <td
            class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
          >
          <i class="fa fa-search-plus" aria-hidden="true"></i>
          </td>
          <td
            class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
          >
          <i class="fa fa-toggle-on" aria-hidden="true" ></i>
          </td>
          <td
            class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
          >
           
            <button
            class="bg-indigo-500 text-white active:bg-indigo-600 text-xs font-bold px-3 py-1 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150"
            type="button"><i class="fa fa-pencil" aria-hidden="true"></i></button>

          </td>
        </tr>
        <tr>
          <th
            class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4 text-left"
          >
            Ortoperdia
          </th>
          <td
            class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
          >
          <i class="fa fa-search-plus" aria-hidden="true"></i>
          </td>
          <td
            class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
          >
          <i class="fa fa-toggle-off" aria-hidden="true"></i>
          </td>
          <td
            class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
          >
          <button
          class="bg-indigo-500 text-white active:bg-indigo-600 text-xs font-bold px-3 py-1 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150"
          type="button"><i class="fa fa-pencil" aria-hidden="true"></i></button>
          </td>
        </tr>
     
      </tbody>
    </table>
  </div>
</div>

</AdminMenu>
