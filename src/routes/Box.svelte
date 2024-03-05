<script>
  import "bootstrap/dist/css/bootstrap.min.css";
  import "../css/Noticias.css";
  import { podcasts } from "../js/podcasts.js";

  // Ordenar los podcasts por fecha (más reciente primero)
  const sortedPodcasts = [...podcasts].sort(
    (a, b) => new Date(b.date) - new Date(a.date)
  );
  // Obtener el podcast más reciente
  const latestPodcast = sortedPodcasts[0];
</script>

<div class="container">
  <h2 class="display-4 mb-4 text-center">Noticias</h2>
</div>
<div class="container">
  <div class="row">
    <div class="col-sm-6">
      <div class="embed-responsive embed-responsive-16by9 ratio ratio-16x9">
        <iframe
          title={"Podcast de " + latestPodcast.title}
          class="embed-responsive-item"
          src={latestPodcast.url}
          allowfullscreen
        ></iframe>
      </div>
    </div>
    <div class="col-sm-6">
      <h2>{latestPodcast.title}</h2>
      <p class="text-justify">{latestPodcast.description}</p>
    </div>
  </div>
</div>

<div class="container mt-5">
  <div class="row">
    <div class="col-md-12 text-center">
      <a href="/podcasts" class="btn btn-dark mx-auto mb-5"
        >Ver más</a
      >
    </div>
  </div>
</div>

<style>
  h2{
  font-family: 'Fira Sans', sans-serif;
  margin-bottom: -.2em;
}
  /* Media query para pantallas pequeñas */
  @media screen and (max-width: 575.98px) {
    .btn {
      font-size: 1.1rem;
      padding: 0.4rem 1rem;
    }
  }
  /* Media query para tablets y pantallas pequeñas */
  @media screen and (min-width: 576px) and (max-width: 767.98px) {
    .btn {
      font-size: 1.2rem;
      padding: 0.5rem 1.5rem;
    }
  }
  /* Media query para pantallas medianas */
  @media screen and (min-width: 768px) and (max-width: 991.98px) {
    .btn {
      font-size: 1.3rem;
      padding: 0.6rem 1.8rem;
    }
  }
  /* Media query para pantallas grandes */
  @media screen and (min-width: 992px) and (max-width: 1199.98px) {
    .btn {
      font-size: 1.4rem;
      padding: 0.7rem 2rem;
    }
  }
  /* Media query para pantallas muy grandes */
  @media screen and (min-width: 1200px) {
    .btn {
      font-size: 1.3rem;
      padding: 0.8rem 2.2rem;
      margin-bottom: 1rem;
      margin-top: -5rem;
    }
  }
  .btn-dark:hover {
    background-color: #fff;
    border-color: #fff;
    color: #000;
  }
</style>