<script>
  import "bootstrap/dist/css/bootstrap.min.css";
  import "../css/Noticias.css";
  import "../routes/Box.svelte";
  import Box from "../routes/Box.svelte";
  export let id = "noticias";

  let pmpalme =
    "https://www.ivoox.com/player_ej_124394773_6_1.html?c1=e5f213%27";
  let bienvenida =
    "https://www.ivoox.com/player_ej_124120144_6_1.html?c1=ebeb75";
</script>

<section {id}>
  <!-- Contenido de la sección "Noticias" -->
  <div class="container">
    <div class="row align-items-center">
      <Box></Box>

    </div>
  </div>
</section>
