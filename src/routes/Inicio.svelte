<!-- Inicio.svelte -->
<script>
  import "bootstrap/dist/css/bootstrap.min.css";
  export let id = "inicio";
</script>

<section {id}>
  <!-- Contenedor para restringir los lados -->
  <div class="container">
    <div class="row align-items-center">
      <div class="col-md-7 order-md-2">
        <img
          src="../src/img/logo-remove.png"
          alt="Logo Rolling The Music"
          class="img-fluid mb-4 animated-image"
        />
      </div>
      <div class="col-md-5 order-md-1">
        <h1 class="display-4 text-uppercase mb-4">Rolling The Music</h1>
        <p class="lead text-justify-lg">
          Somos un programa de música que tiene como finalidad ayudar a los
          cantantes emergentes a darse a conocer. En los capítulos podrás
          encontrar entrevistas a cantantes y profesionales de la música entre
          otros. Nuestro objetivo es transmitir nuestra pasión por la música y
          por el talento joven ofreciendo una variedad de contenidos a través
          del podcast y de redes sociales. ¡Podrás escucharnos semanalmente!
        </p>
      </div>
    </div>
  </div>
</section>

<style>
  .animated-image {
    animation: slideInRight 1s ease-in-out;
  }

  @keyframes slideInRight {
    0% {
      opacity: 0;
      transform: translateX(100%);
    }
    100% {
      opacity: 1;
      transform: translateX(0);
    }
  }
  /* Alineación justificada solo para pantallas grandes */
  .text-justify-lg {
    text-align: justify;
  }
</style>
