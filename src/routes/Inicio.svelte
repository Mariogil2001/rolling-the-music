<!-- Inicio.svelte -->
<script>
  import "bootstrap/dist/css/bootstrap.min.css";
  export let id = "inicio";
  import logo from "../img/logo-remove.png";
</script>

<section id={id}>
  <!-- Contenedor para restringir los lados -->
  <div class="container">
    <div class="row align-items-center">
      <div class="text-center">
        <h1 class="display-2">Rolling The Music</h1>
      </div>
      <div class="col-md-5 col-lg-6 order-md-2 order-lg-1 text-center">
        <img
          src={logo}
          alt="Logo Rolling The Music"
          class="img-fluid mb-4" width="400px"
        />
      </div>
      <div class="col-md-7 col-lg-6 order-md-1 order-lg-2">
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

h1{
  font-family: 'Fira Sans', sans-serif;
  margin-bottom: -.2em;
}
@media only screen and (max-width: 576px) {
  h1:first-child{
    display: none;
  }
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
  .text-justify-lg {
    text-align: justify;
  }
</style>
