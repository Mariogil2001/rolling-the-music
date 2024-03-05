<script>
  import "bootstrap/dist/css/bootstrap.min.css";
  import "../css/Noticias.css";
  import "../routes/Box.svelte";
  import Box from "../routes/Box.svelte";
  export let id = "noticias";

</script>

<section {id}>
  <!-- Contenido de la sección "Noticias" -->
  <div class="container">
    <div class="row align-items-center">
      <Box></Box>

    </div>
  </div>
</section>
