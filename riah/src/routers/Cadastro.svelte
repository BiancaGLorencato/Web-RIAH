<script>
  import A from "../components/A.svelte";
  
  import Button from "../components/Button.svelte";
import Footer from "../components/Footers/Footer.svelte";
  
  import Input from "../components/Input.svelte";
  
  import LogoLogin from "../components/LogoLogin.svelte";
  
  let email, password;
  
  function entrar(){
      console.log(email);
  }
  
  </script>
  
  <div class="container flex bg-gray-900 justify-center items-center w-screen h-screen mx-auto">
  <section class="text-gray-400  body-font overflow-hidden">
      <div class="container px-5 py-24 mx-auto">
        <div class="lg:w-4/5 mx-auto flex flex-wrap">
         <LogoLogin></LogoLogin>
          
          <form 
              class="lg:w-1/2 w-full bg-gray-800 bg-opacity-50 rounded-lg p-8  lg:pl-10 lg:py-6 mt-6 lg:mt-0">
  
                  <h2 class="text-white text-lg font-medium title-font mb-5">Login</h2>
                  <Input label="Email" bind:value={email} type="text" />
                  <Input label="Senha" bind:value={password} type="password" />
                  <Button on:click|once={entrar}>Entrar</Button>
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
  

