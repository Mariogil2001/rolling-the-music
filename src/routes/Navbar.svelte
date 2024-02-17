<!-- Navbar.svelte -->
<script>
import '../css/Navbar.css';
import { onMount } from 'svelte';

onMount(() => {
    window.addEventListener('scroll', handleScroll);
    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  });

  function handleScroll() {
    const navbar = document.querySelector('nav');
    if (window.scrollY > 0) {
      navbar.classList.add('navbar-blur');
    } else {
      navbar.classList.remove('navbar-blur');
    }
  }

  function scrollIntoView(event) {
    const targetId = event.target.getAttribute("href");
    const targetElement = document.querySelector(targetId);
    console.log("ID:", targetId); // Aquí se muestra el identificador en la consola
    if (targetElement) {
      event.preventDefault();
      targetElement.scrollIntoView({ behavior: "smooth" });
    }
  }
</script>

<nav>
  <div>
    <a href="#inicio" on:click|preventDefault={scrollIntoView}>Inicio</a>
    <a href="#noticias" on:click|preventDefault={scrollIntoView}>Noticias</a>
    <a href="#contacto" on:click|preventDefault={scrollIntoView}>Contacto</a>
  </div>
</nav>


