<script>
    import InputDois from "../../../components/Elements/InputDois.svelte";
import Radio from "../../../components/Elements/Radio.svelte";
import Select from "../../../components/Elements/Select.svelte";
import AdminMenu from "../../../components/Headers/AdminMenu.svelte";
    
    
let         logo = sessionStorage.logo;
    
       let  titule = "";
       let headers = ['Nome', 'Informações', 'status', ' '];
       let options = [
            {
                id:'1', name:'Teste'
            }
       ]
</script>
    
 <AdminMenu logo={logo}>
    <div class="flex flex-wrap">
        <div class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded-lg border-0">
            <div class="rounded-t bg-black mb-0 px-6 py-6">
                <div class="text-center flex justify-between">
                    <h6 class="text-white text-xl font-bold">Nova urgência</h6>
                </div>
                <div class="text-center flex justify-end">
                    <button class="bg-red-400 text-white active:bg-red-500 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 ease-linear transition-all duration-150" type="button"> Cancelar </button>
                    <button class="bg-blue-400 text-white active:bg-blue-500 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 ease-linear transition-all duration-150" type="button"> Salvar </button>
                </div>
            </div>
            <div class="flex-auto bg-white px-4 lg:px-10 py-10 pt-0">
                <form>
                <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase">
                    Urgência Informação
                </h6>
                <div class="flex flex-wrap">
                    <div class="w-full lg:w-6/12 px-4">
                        <InputDois label="Nome" id="name" type="text" classes="mb-3"></InputDois>
                </div>
            <div class="w-full lg:w-6/12 px-4">
                <label class="block uppercase text-blueGray-600 text-xs font-bold mb-2">Status</label>
                <Radio info="Ativo" id="status" type="checkbox" classes="mb-3"></Radio>
            </div>
      </div>

      <hr class="mt-6 border-b-1 border-blueGray-300" />

      <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase">
        Ação da nova Urgência
      </h6>
      <div class="flex flex-wrap">
        
        <div class="w-full lg:w-6/12 px-4">
            <div class="relative w-full mb-3">
                <label class="block uppercase text-blueGray-600 text-xs font-bold mb-2">Triagem</label>
                <Radio info="Sim"  id="triagem_sim" name="triagem" type="radio" classes="mb-3"></Radio>
                <Radio info="Não"  id="triagem_não" name="triagem" type="radio" classes="mb-3"></Radio>
            </div>
        </div>
        <div class="w-full lg:w-6/12 px-4">
            <Select label="Escolher especialidade para encaminhar" options="{options}" id="prox_especialidade"  classes="mb-3"></Select>
        </div>
      </div>

      <hr class="mt-6 border-b-1 border-blueGray-300" />

    </form>
  </div>
</div>

    </div>
 </AdminMenu>