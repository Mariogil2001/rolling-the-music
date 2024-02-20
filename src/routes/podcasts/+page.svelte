<script>
  import { podcasts } from '../../js/podcasts';
  import "bootstrap/dist/css/bootstrap.min.css";
  import "../../css/Noticias.css";

  function formatDate(date) {
    const d = new Date(date);
    const day = String(d.getDate()).padStart(2, '0');
    const month = String(d.getMonth() + 1).padStart(2, '0'); // January is 0!
    const year = d.getFullYear();

    return `${day}-${month}-${year}`;
  }
</script>

<div class="col-md-7">
  <h3 class="display-4 text-uppercase mb-4">Todos los Podcasts</h3>
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