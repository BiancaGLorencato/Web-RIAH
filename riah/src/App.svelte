<script>
	import Router from 'svelte-spa-router';
	import Cadastro from './routers/Cadastro.svelte';
	import Dashboard from './routers/Administrador/Dashboard.svelte';
	import Home from './routers/Home.svelte';
	import Login from './routers/Login.svelte';

	import "/app.css";
import Urgencias from './routers/Administrador/Urgencia/Urgencias.svelte';
import UrgenciaNovo from './routers/Administrador/Urgencia/UrgenciaNovo.svelte';


let routes = {
	"/": Home,
	"/home/:hospital": Home, 
	"/cadastro" : Cadastro,
	"/login" : Login,
	"/dashboard": Dashboard,
	"/admin/urgencia": Urgencias,
	"/admin/urgencia/novo": UrgenciaNovo
}

</script>

<style global lang="postcss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
  </style>
	
<main>
	<Router {routes} />
	<slot/>
</main>