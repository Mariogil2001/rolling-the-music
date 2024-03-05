<script>
  import Navbar from "./Navbar.svelte";
  import Contacto from "./Contacto.svelte";
  import "bootstrap/dist/css/bootstrap.min.css";
  import "../css/Navbar.css";
</script>

<body class="app">
  <Navbar />
  <div class="container">
    <main>
      <slot />
    </main>
    <Contacto />
  </div>
</body>

<style>
  @media only screen and (min-width: 576px) {
    main > * {
      margin-inline: 120px !important;
    }
  }
  @font-face {
    font-family: "Fira Sans";
    font-style: normal;
    font-display: swap;
    font-weight: 400;
    src:
      url(https://cdn.jsdelivr.net/fontsource/fonts/fira-sans@latest/latin-400-normal.woff2)
        format("woff2"),
      url(https://cdn.jsdelivr.net/fontsource/fonts/fira-sans@latest/latin-400-normal.woff)
        format("woff");
    unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA,
      U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+2074, U+20AC, U+2122,
      U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
  }

  /* Agrega estilos generales para tu aplicación aquí si es necesario */
  body {
    margin-top: 7em;
    background-color: #c8b6ff;
    font-family: "Times New Roman", Times, serif;
  }

  /* Media query para pantallas pequeñas */
  @media screen and (max-width: 600px) {
    body {
      margin-top: 5em; /* Reducción del margen superior en pantallas pequeñas */
    }
  }
</style>
