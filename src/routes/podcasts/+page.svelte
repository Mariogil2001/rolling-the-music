<script>
  import { podcasts } from '../../js/podcasts';
  import "bootstrap/dist/css/bootstrap.min.css";
  import "../../css/Noticias.css";

  function formatDate(date) {
    const formatter = new Intl.DateTimeFormat('es', { dateStyle: 'long' })
    return formatter.format(new Date(date))
  }
</script>

<div class="container">
  <h1 class="mb-4 text-center align-content-center">Todos los Podcasts</h1>
</div>

<div class="container">
  {#each podcasts as podcast}
    <div class="row mb-5">
      <div class="col-md-6">
        <div class="embed-responsive embed-responsive-16by9 ratio ratio-16x9">
          <iframe
            title={'Podcast de ' + podcast.title}
            class="embed-responsive-item"
            src={podcast.url}
            allowfullscreen
          ></iframe>
        </div>
      </div>
      <div class="col-md-6">
        <h2>{podcast.title}</h2>
        <p class="text-justify">{podcast.description}</p>
        <p class="text-muted">Fecha: {formatDate(podcast.date)}</p>
      </div>
    </div>
  {/each}
</div>
<style>
  h1{
    font-family: 'Fira Sans', sans-serif;
  }
</style>