<script>
import { bind } from "svelte/internal";
import A from "../components/A.svelte";
import axios from 'axios'; 
import Button from "../components/Button.svelte";
import Error from "../components/Error.svelte";
import Footer from "../components/Footers/Footer.svelte";

import Input from "../components/Input.svelte";

import LogoLogin from "../components/LogoLogin.svelte";
import MensagemSucesso from "../components/MensagemSucesso.svelte";


let email, password, errorMensagem, errorLogin, mensagemLogin, sucesso;

let errorSesion = false;

let hospital = sessionStorage.token;
if(hospital == undefined){
  errorSesion = true;
  errorMensagem = "Nem hospital foi escolhido. Por favor escolher uma instituição"
}

/*sessionStorage.removeItem("enkot");

async function entrar(){
        try{
            const response = await axios.post('http://127.0.0.1:8000/api/login',{
              "token_hospital": hospital,
              "email": email,
              "password": password
            });
            errorLogin = false;
            console.log(response.data);
            sessionStorage.removeItem("enkot");
            sessionStorage.setItem("enkot", response.data.token);
            mensagemLogin = "Bem vindo";
            sucesso = true;
            if(response.data.perfil == 'admin'){
              setTimeout(function() {
    window.location.href = "/#/dashboard";
}, 2000);
            }
        }catch(erro){
            console.error(erro);
            errorLogin = true;
            sucesso = false;
            mensagemLogin = erro.response.data.mensagem;
            email="";
            password="";
        }
    }*/

</script>
{#if errorSesion }
  <Error mensagem={errorMensagem}/>
{:else}
{#if errorLogin }
<Error mensagem={mensagemLogin}/>
{/if}
<div class="container flex bg-gray-900 justify-center items-center w-screen h-screen mx-auto">
<section class="text-gray-400  body-font overflow-hidden">
    <div class="container px-5 py-24 mx-auto">
      <div class="lg:w-4/5 mx-auto flex flex-wrap">
       <LogoLogin></LogoLogin>
        {#if sucesso}
          <MensagemSucesso sucesso={mensagemLogin}/>
        {/if}
        <form  
            class="lg:w-1/2 w-full bg-gray-800 bg-opacity-50 rounded-lg p-8  lg:pl-10 lg:py-6 mt-6 lg:mt-0">

                <h2 class="text-white text-lg font-medium title-font mb-5">Login</h2>
                <Input label="Email" bind:value={email} type="text" />
                <Input label="Senha" bind:value={password} type="password" />
                <div class="relative mb-4 text-center">
                <button  type="submit"
                class="text-white bg-indigo-500 border-0 py-2 px-5 focus:outline-none hover:bg-indigo-600 rounded text-lg">
                Entrar</button>
              </div>
                <div class="relative mb-4">
                    <hr />
                </div>
          
                <A href="/#/cadastro" class="text-gray-400">Crie sua conta</A>
          
            </form>
      </div>
    </div>
    <Footer></Footer>
  </section>

</div>
{/if}
