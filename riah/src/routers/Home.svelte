<script> 
    import axios from 'axios'; 
import Error from '../components/Error.svelte';
    export let params = {};

    let error = false;
    let mensagem = "";
    

    /*async function iniciar(){
        try{
            const response = await axios.get('http://127.0.0.1:8000/api/home/'+params.hospital);
            sessionStorage.removeItem("token");
            sessionStorage.setItem("token", response.data.token);
            sessionStorage.removeItem("logo");
            sessionStorage.setItem("logo", response.data.url)
        }catch(erro){
            console.error(erro);
            error = true;
            sessionStorage.removeItem("token");
            sessionStorage.removeItem("logo");
            mensagem = erro.response.data.mensagem;
        }
    }

    if(params.hospital == undefined){
        error = true;
        mensagem = "Nem hospital foi escolhido. Por favor escolher uma instituição";

    }else{
        iniciar();

    }*/



</script>
<div>
{#if error}
    <Error mensagem={mensagem} />
{:else}
<a href="/#/login">Login</a>
<a href="/#/cadastro">Cadastro</a>
{/if}
</div>