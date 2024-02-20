<script>
	import Navbar from './Navbar.svelte';
    import Contacto from './Contacto.svelte';
    import "bootstrap/dist/css/bootstrap.min.css";
    import "../css/Navbar.css";
</script>

<body class="app">
	<Navbar />
    <div class="container">
	<main>
		<slot />
	</main>
    <Contacto />

</div>
</body>

<style>
    @media only screen and (min-width: 576px) {
       main > *{
        margin-inline: 120px !important;
    }

}

    /* Agrega estilos generales para tu aplicación aquí si es necesario */
    body {
        margin-top: 7em;
        background-color: #c8b6ff;
        font-family: 'Times New Roman', Times, serif;
        
    }

    /* Media query para pantallas pequeñas */
    @media screen and (max-width: 600px) {
        body {
            margin-top: 5em; /* Reducción del margen superior en pantallas pequeñas */
        }
    }
</style>