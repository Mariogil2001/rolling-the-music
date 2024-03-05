<script>
  import { fade } from "svelte/transition";
  import "bootstrap/dist/css/bootstrap.min.css";
  export let id = "contacto";
  import check from "../img/check.svg";
  import mail from "../img/mail.svg";
  import instagram_logo from "../img/instagram_icon.svg";
  const instagram = "https://www.instagram.com/rollingthemusic/";

  let mostrarCorreo = false; // Variable de estado para controlar qué imagen mostrar en el botón de correo
  let timeout;

  // Función para cambiar la imagen del botón de correo y mostrar/ocultar el texto del correo
  function cambiarImagenCorreo() {
    mostrarCorreo = !mostrarCorreo;
    clearTimeout(timeout);
    timeout = setTimeout(() => {
      mostrarCorreo = !mostrarCorreo;
    }, 1000); // Cambiar de nuevo a la imagen original después de 2 segundos
  }

  // Función para copiar el correo electrónico al portapapeles
  function copiarCorreo() {
    const correo = "contactrollingthemusic@gmail.com"; // Aquí debes colocar tu dirección de correo electrónico
    navigator.clipboard
      .writeText(correo)
      .then(() => {
        cambiarImagenCorreo(); // Cambiar la imagen del botón de correo
      })
      .catch((err) => {
        console.error("Error al copiar el correo electrónico: ", err);
      });
  }
</script>

<section {id}>
  <div class="container">
    <div class="row align-items-center justify-content-center">
      <div class="col-md-5 text-center">
        <h3 class="display-4 text-uppercase mb-4">Contacto</h3>
        <div class="d-flex align-items-center justify-content-center mb-4">
          <!-- Botón para Instagram -->
          <a href={instagram} target="_blank" class="me-4 btn-correo">
            <img src={instagram_logo} alt={instagram} style="width: 40px;" />
          </a>
          <!-- Botón para copiar correo electrónico -->
          <!-- svelte-ignore a11y-invalid-attribute -->
          <a
            href="javascript:void(0);"
            on:click|preventDefault={copiarCorreo}
            class="btn-correo" id="correo"
          >
            {#if mostrarCorreo}
              <img src={check} alt="Correo Copiado" style="width: 40px;" />
            {:else}
              <img src={mail} alt="Correo Original" style="width: 40px;" />
            {/if}
          </a>
        </div>
        <p
          class="lead mb-5 email-link"
          onclick="location.href='mailto:contactrollingthemusic@gmail.com';"
        >
          contactrollingthemusic@gmail.com
        </p>
      </div>
    </div>
  </div>
</section>

<style>

p{
  cursor: pointer;
}
  /* Estilos de transición */
  .fade {
    transition:
      opacity 0.5s ease,
      transform 0.5s ease;
  }

  .fade-in {
    opacity: 1;
    transform: translateY(0);
  }

  .fade-out {
    opacity: 0;
    transform: translateY(-20px);
  }

  /* Estilos para el texto del correo */
  button span {
    margin-left: 10px; /* Ajusta el espacio entre el icono y el texto */
  }

  /* Estilos para el botón de correo al hacer hover */
  .btn-correo:hover img {
    filter: brightness(0) invert(1); /* Cambia el color del icono a blanco al hacer hover */
  }
</style>
