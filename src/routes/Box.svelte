<script>
  import "bootstrap/dist/css/bootstrap.min.css";
  import "../css/Noticias.css";
  let pmpalme =
    "https://www.ivoox.com/player_ej_124394773_6_1.html?c1=e5f213%27";
  let bienvenida =
    "https://www.ivoox.com/player_ej_124120144_6_1.html?c1=ebeb75";
</script>

<div class="col-md-7">
  <h3 class="display-4 text-uppercase mb-4">Noticias</h3>
</div>
<div class="container">
  <div class="row">
    <div class="col-md-6">
      <div class="embed-responsive embed-responsive-16by9 ratio ratio-16x9">
        <iframe
          title="Podcast PM Palme"
          class="embed-responsive-item"
          src={pmpalme}
          allowfullscreen
        ></iframe>
      </div>
    </div>
    <div class="col-md-6">
      <h2>PM Palme</h2>
      <p class="text-justify">
        THoy entrevistamos a Víctor, cantante de Peme Palme, un grupo con un
        toque veraniego y muy buen rollo, con canciones pegadizas y con mucho
        ritmo. Su trayectoria empezó en 2017 en Cullera, un lugar que les ha
        inspirado para componer sus canciones. ¡Escúcha sus inicios y sus
        consejos! Además, hoy hay una sección especial en la que tendrás que
        adivinar si el nombre de una banda es ficticio o de los noventa, ¿crees
        que existió No me pises que llevo chanclas? o ¿Písame que llevo
        converse?
      </p>
    </div>
  </div>
</div>

<div class="container">
  <div class="row">
    <div class="col-md-6">
      <div class="embed-responsive embed-responsive-16by9 ratio ratio-16x9">
        <iframe
          title="Podcast de Bienvenida"
          class="embed-responsive-item"
          src={bienvenida}
          allowfullscreen
        ></iframe>
      </div>
    </div>
    <div class="col-md-6">
      <h2>¡Bienvenida!</h2>
      <p class="text-justify">
        ¡Hola! Somos Julia y Maya, estudiantes de periodismo y comunicación
        audiovisual. Tenemos muchas ganas e ilusión por realizar este podcast
        donde entrevistaremos a cantantes emergentes y profesionales de la
        música. Escúchanos para conocer nuestra historia y motivaciones para
        realizar Rolling The Music y ayudar a que los jóvenes cantantes puedan
        alcanzar su sueño. Somos estudiantes universitarias con motivación y
        pasión por la música.
      </p>
    </div>
  </div>
</div>
