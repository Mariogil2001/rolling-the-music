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

</script>

<nav>
  <div>
    <a href="/" >Inicio</a>
    <a href="/podcasts">Podcasts</a>
  </div>
</nav>


