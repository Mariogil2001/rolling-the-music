<!-- App.svelte -->
<script>
    import Navbar from './Navbar.svelte';
    import Inicio from './Inicio.svelte';
    import Noticias from './Noticias.svelte';
    import Contacto from './Contacto.svelte';
</script>

<style>
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

<body>
    <Navbar />
    <Inicio />
    <Noticias />
    <Contacto />
</body>
