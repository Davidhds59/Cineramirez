<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home - Winetflix</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <link rel="stylesheet" href="home_mejorado.css">
   
   <!-- slider scrip -->
   <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- enlace-a-los-stylos-css -->
    <link rel="stylesheet" href="">
    <!-- enlace-a-otros-stylos-css -->
    <!-- CSS only -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    
    
    <!-- JavaScript Bundle with Popper -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
    <!-- fin slider scrip -->
    
</head>
<style> 
/* Estilos del splash screen */
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}


@keyframes fadeIn {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}


/* Reset de estilos por defecto */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: black;
    color: #ffffff;
    line-height: 1.6;
    overflow-x: hidden; /* Evita el scroll horizontal */
}

/* Estilo del encabezado */
header {
    background-color: black;
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    overflow-x: hidden; /* Evita el scroll horizontal en el header */
}

header h1 {
    font-size: 14px;
    color: #FFF;
}

/* Estilos para el menú horizontal */
nav ul {
    list-style: none;
    display: flex;
    gap: 15px; /* Espacio entre los elementos del menú */
    padding: 0;
    margin: 0;
    overflow-x: auto; /* Permite el desplazamiento horizontal */
    white-space: nowrap; /* Evita el salto de línea en los elementos */
    width: 100%; /* Asegura que ocupe todo el ancho disponible */
    cursor: grab; /* Cambia el cursor para indicar que se puede arrastrar */
}

nav ul:active {
    cursor: grabbing; /* Cambia el cursor cuando se está arrastrando */
}

nav ul::-webkit-scrollbar {
    height: 6px; /* Tamaño de la barra de desplazamiento */
}

nav ul::-webkit-scrollbar-thumb {
    background-color: #37475a; /* Color del "thumb" de la barra de desplazamiento */
    border-radius: 5px; /* Bordes redondeados */
}

nav ul::-webkit-scrollbar-track {
    background-color: #232f3e; /* Color del track de la barra de desplazamiento */
    border-radius: 5px; /* Bordes redondeados */
}

nav ul li {
    flex: 0 0 auto;
}

nav ul li:last-child {
    margin-left: auto; /* Empuja el último elemento a la derecha */
}

nav ul li a {
    color: #ffffff;
    text-decoration: none;
    padding: 10px 15px;
    transition: background-color 0.3s ease, color 0.3s ease;
    border-radius: 46px;
}

nav ul li a.active,
nav ul li a:hover {
    background-color: #2b3848;
    color: #ffffff;
}

nav ul::-webkit-scrollbar {
    display: none; /* Oculta la barra de desplazamiento en navegadores basados en Webkit */
}

nav {
    width: 100%; /* Asegura que el contenedor del nav se expanda a lo largo de toda la pantalla */
}

/* Para mejorar la accesibilidad, puede ser útil tener un ligero padding alrededor de los items del menú */
nav ul li a {
    display: block;
}

/* Asegura que el menú sea más responsivo */
@media (max-width: 600px) {
    nav ul {
        flex-direction: column; /* Cambia la dirección a columna para dispositivos muy pequeños */
    }

    nav ul li a {
        padding: 10px; /* Ajusta el padding según sea necesario */
    }
}

/* Estilo del cuerpo principal */
main {
    padding: 5px 5px; /* Ajusta el padding superior/inferior a 2px y derecho/izquierdo a 3px */
}


.seccion {
    display: none;
}

.seccion.active {
    display: block;
}

.categoria {
    margin-bottom: 20px;
}

.categoria h3 {
    margin-bottom: 10px;
    font-size: 20px;
    color: #FFF;
}

.categoria-container {
    display: flex;
    gap: 10px;
    overflow-x: auto;
    padding-bottom: 10px;
    scroll-behavior: smooth;
}

.categoria-container::-webkit-scrollbar {
    height: 6px;
}

.categoria-container::-webkit-scrollbar-thumb {
    background-color: #37475a;
    border-radius: 5px;
}

.categoria-container::-webkit-scrollbar-track {
    background-color: #232f3e;
    border-radius: 5px;
}

.item-peli, .item-serie, .item-anime {
    flex: 0 0 auto;
    width: 150px;
    cursor: pointer;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    position: relative;
    background-color: #232f3e;
    border-radius: 5px;
    overflow: hidden;
}

.item-peli img, .item-serie img, .item-anime img {
    width: 100%;
    height: 205px; /* Ajusta la altura según sea necesario */
    object-fit: cover;
    border-radius: 7px 7px 0 0;
}

.item-peli:hover, .item-serie:hover, .item-anime:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.item-peli h3, .item-serie h3, .item-anime h3 {
    font-size: 10px;
    margin: 0;
    padding: 5px;
    color: #ffffff;
    text-align: center;
    background: rgba(0, 0, 0, 0.7);
    border-radius: 0 0 5px 5px;
    position: absolute;
    bottom: 0;
    width: 100%;
}

.calidad {
    font-size: 12px;
    color: #0076c9;
    position: absolute;
    top: 5px;
    right: 5px;
    background: rgba(0, 0, 0, 0.7);
    padding: 2px 5px;
    border-radius: 3px;
}

/* Ajustes */
#ajustes ul {
    list-style: none;
    padding: 0;
}

#ajustes ul li {
    margin-bottom: 10px;
}

#ajustes ul li a {
    color: #ffffff;
    text-decoration: none;
    padding: 10px;
    display: block;
    background-color: #37475a;
    border-radius: 5px;
    transition: background-color 0.3s ease, color 0.3s ease;
}

#ajustes ul li a:hover {
    background-color: #566f8d;
    color: #f9a825;
}

/* Media queries para pantallas pequeñas */
@media (max-width: 768px) {
    header {
        flex-direction: column;
        align-items: flex-start;
    }

    nav ul {
        flex-direction: row;
        overflow-x: auto;
        width: 100%;
        white-space: nowrap; /* Evita el salto de línea en los elementos */
    }

    nav ul li {
        display: inline-block;
    }

    nav ul li a {
        display: block;
        text-align: center;
        padding: 10px;
        margin: 5px 0;
    }

    .categoria-container {
        flex-wrap: nowrap;
        overflow-x: scroll;
    }

    .item-peli, .item-serie, .item-anime {
        width: 120px;
    }
}


<!-- slider  -->
    /* stylos para ajustar el carousel */
.carousel.pointer-event {
    touch-action: pan-y;
    width: 100%;
    height: 10rem;
    top: 0.2rem;
}
.carousel-inner {
    position: relative;
    width: 100%;
    height: 10rem;
    overflow: hidden;
}
.carousel-item {
    width: 100%;
    padding: 2px 6px;
    height: 10rem;
}
.carousel-item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    padding: 4px;
    border-radius: 12px;
}
.carousel-item h6 {
    position: absolute;
    background: #00000094;
    color: #f0f8ff;
    outline: 1px solid #ffffffb8;
    left: 1rem;
    top: 1rem;
    width: 34%;
    height: 16%;
    display: grid;
    justify-items: center;
    align-items: center;
    margin: 0;
    padding: 0;
    border-radius: 4px;
}
/* stylos para ajustar el carousel */



<!-- fin slider -->

	</style> 
	<!-------- aquí cambias el logo de inicio y titulo------->
<body>
	
        </div>
    </div>
    <header>
       
        <nav>
            <ul>
                <li><a href="go:buscador"><i class="fas fa-search"></i>  </a></li>
                <li><a href="#" id="mostrar-peliculas"><i class="fas fa-film"></i> Movies </a></li>
                <li><a href="#" id="mostrar-series"><i class="fas fa-tv"></i> Series</a></li>
                <li><a href="go:tvfree" id="mostrar-animes"><i class="fas fa-fire"></i> Tv </a></li>
              

  <li><a href="#" id="mostrar-ajustes"><i class="fas fa-cog"></i> Ajustes</a></li>
                
            </ul>
        </nav>
    </header>
    
    
   <!-- posible slider -->
    <!-- area para el cousel de bootstrap -->
    <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner">
          <div class="carousel-item active">
              <h6>TENDENCIA</h6>
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQZK60C2gtP6DEs4jt80WW-KgE2sJxU4cHZaA&usqp=CAU" class="d-block w-100" alt="banner">
          </div>
          <div class="carousel-item">
            <h6>TENDENCIA</h6>
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTsacxLhPdsqqD9I9K_aLSo_8pPcIrFR4cQZh_WR474LKA6P489DFe6pJ05&s=10" class="d-block w-100" alt="banner">
          </div>
          <div class="carousel-item">
            <h6>TENDENCIA</h6>
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTloQDb0nag-Zso4qbDBgmJyDqg93iGnjMXROwfid8agHn92A1LXsImcFE&s=10" class="d-block w-100" alt="banner">
          </div>
        </div>
    </div>
    
    <!-- fin slider -->
    
    <main>
        <section id="peliculas" class="seccion active">
            <h2>Películas</h2>
        </section>

        <section id="series" class="seccion">
            <h2>Series</h2>
        </section>

        

        <section id="ajustes" class="seccion">
            <h2>Ajustes</h2>
            <ul>
                <li><a href="https://api.whatsapp.com/send?text=https://miniurl.cl/AppPeliculasCR">Compartir WhatsApp</a></li>
                <li><a href="https://www.facebook.com/sharer/sharer.php?u=https://miniurl.cl/AppPeliculasCR">Compartir Facebook</a></li>
                <li><a href="https://t.me/peliculas2024cine">Pedidos</a></li>
                <li><a href="https://www.pelismx.lat/">Pagina Web </a></li>
                <li><a href="https://miniurl.cl/PaypalDonation" target="_blank">Donaciones</a></li>
                 <li><a href="go:tuto" target="_blank">Como Ver En La TV (Chromecast)</a></li>
   
 <li><a href="go:dp" target="_blank">Como Descargar Una Película </a></li>

<li><a href="go:dmca" target="_blank"> DMCA </a></li>

            </ul>
        </section>
    </main>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const token = 'mxlat';
            const nombreJSON = 'PELISMX';
            mostrarSeccion('peliculas');
            obtenerYMostrarJSON(token, nombreJSON); 
            obtenerYMostrarSeries(token, nombreJSON);
            obtenerYMostrarAnimes(token, nombreJSON);
        
            document.getElementById('mostrar-peliculas').addEventListener('click', () => mostrarSeccion('peliculas'));
            document.getElementById('mostrar-series').addEventListener('click', () => mostrarSeccion('series'));
            document.getElementById('mostrar-animes').addEventListener('click', () => mostrarSeccion('animes'));
            document.getElementById('mostrar-ajustes').addEventListener('click', () => mostrarSeccion('ajustes'));
        
            function mostrarSeccion(seccion) {
                document.querySelectorAll('main section').forEach(sec => {
                    sec.style.display = 'none';
                });
                document.getElementById(seccion).style.display = 'block';
                document.querySelectorAll('nav ul li a').forEach(enlace => {
                    enlace.classList.remove('active');
                });
                document.getElementById(`mostrar-${seccion}`).classList.add('active');
            }
        });
        
        const apiUrl = 'https://mediapanel.site/dashboard/api_movie.php';
        const apiUrlSeries = 'https://mediapanel.site/dashboard/api_series.php';
        const apiUrlAnimes = 'https://mediapanel.site/dashboard/api_animes.php';

        async function obtenerYMostrarJSON(token, nombreJSON) {
            try {
                const response = await fetch(`${apiUrl}?token=${token}&json=${nombreJSON}`);
                if (response.ok) {
                    const data = await response.json();
                    mostrarPeliculas(data.movies);
                } else {
                    console.error('Error al obtener el JSON de películas:', response.statusText);
                }
            } catch (error) {
                console.error('Error al obtener el JSON de películas:', error);
            }
        }

        function mostrarPeliculas(peliculas) {
            const peliculasPorCategoria = agruparPorCategoria(peliculas);
            const peliculasSection = document.getElementById('peliculas');
            peliculasSection.innerHTML = '';

            const categoriasOrdenadas = Object.keys(peliculasPorCategoria).sort((a, b) => {
                if (a === 'Estrenos') return -1;
                if (b === 'Estrenos') return 1;
                return 0;
            });

            categoriasOrdenadas.forEach(categoria => {
                const categoriaDiv = document.createElement('div');
                categoriaDiv.classList.add('categoria');
                categoriaDiv.innerHTML = `<h3>${categoria}</h3>`;

                const categoriaContainer = document.createElement('div');
                categoriaContainer.classList.add('categoria-container');

                peliculasPorCategoria[categoria].reverse().forEach(pelicula => {
                    const movieCard = `
                        <div class="item-peli" data-tmdb-id="${pelicula.id_tmdb}">
                            <img src="${pelicula.url_imagen}" alt="${pelicula.titulo}">
                            <h3>${pelicula.titulo}</h3>
                            <p class="calidad">${pelicula.calidad}</p>
                        </div>
                    `;
                    categoriaContainer.insertAdjacentHTML('beforeend', movieCard);
                });

                categoriaDiv.appendChild(categoriaContainer);
                peliculasSection.appendChild(categoriaDiv);
            });

            document.querySelectorAll('.item-peli').forEach(item => {
                item.addEventListener('click', function() {
                    const tmdbId = this.getAttribute('data-tmdb-id');
                    localStorage.setItem('tmdbId', tmdbId);
                    window.location.href = 'go:peliculas';
                });
            });
        }

        async function obtenerYMostrarSeries(token, nombreJSON) {
          try {
              const response = await fetch(`${apiUrlSeries}?token=${token}&json=${nombreJSON}`);
              if (response.ok) {
                  const data = await response.json();
                  mostrarSeries(data.series);
              } else {
                  console.error('Error al obtener el JSON de series:', response.statusText);
              }
          } catch (error) {
              console.error('Error al obtener el JSON de series:', error);
          }
      } 
      
      function mostrarSeries(series) {
        const seriesPorCategoria = agruparPorCategoria(series);
    
        const seriesSection = document.getElementById('series');
        seriesSection.innerHTML = '';
    
        // Ordenar las categorías para que 'Estrenos' sea la primera
        const categoriasOrdenadas = Object.keys(seriesPorCategoria).sort((a, b) => {
            if (a === 'Estrenos') return -1; // 'Estrenos' primero
            if (b === 'Estrenos') return 1; // 'Estrenos' primero
            return 0;
        });
    
        categoriasOrdenadas.forEach(categoria => {
            const categoriaDiv = document.createElement('div');
            categoriaDiv.classList.add('categoria');
            categoriaDiv.innerHTML = `<h3>${categoria}</h3>`;
    
            const categoriaContainer = document.createElement('div');
            categoriaContainer.classList.add('categoria-container');
    
            // Ordenar las series al revés (de más reciente a más antiguo)
            seriesPorCategoria[categoria].reverse().forEach(serie => {
                const serieCard = `
                    <div class="item-serie" data-tmdb-id="${serie.id_tmdb}">
                        <img src="${serie.url_imagen}" alt="${serie.titulo}">
                        <h3>${serie.titulo}</h3>
                    </div>
                `;
                categoriaContainer.insertAdjacentHTML('beforeend', serieCard);
            });
    
            categoriaDiv.appendChild(categoriaContainer);
            seriesSection.appendChild(categoriaDiv);
        });
    
        // Event listener para cada serie
        document.querySelectorAll('.item-serie').forEach(item => {
            item.addEventListener('click', function() {
                const tmdbId = this.getAttribute('data-tmdb-id');
                localStorage.setItem('tmdbId', tmdbId);
                window.location.href = 'go:series';
            });
        });
    }
    
      
      async function obtenerYMostrarAnimes(token, nombreJSON) {
          try {
              const response = await fetch(`${apiUrlAnimes}?token=${token}&json=${nombreJSON}`);
              if (response.ok) {
                  const data = await response.json();
                  if (data.anime) {
                      mostrarAnimes(data.anime);
                  } else {
                      console.error('El objeto "anime" está vacío o no está definido en la respuesta del servidor.');
                  }
              } else {
                  console.error('Error al obtener el JSON de animes:', response.statusText);
              }
          } catch (error) {
              console.error('Error al obtener el JSON de animes:', error);
          }
      }
      
      function mostrarAnimes(anime) {
        const animesPorCategoria = agruparPorCategoria(anime);
    
        const animesSection = document.getElementById('animes');
        animesSection.innerHTML = '';
    
        // Ordenar las categorías para que 'Estrenos' sea la primera
        const categoriasOrdenadas = Object.keys(animesPorCategoria).sort((a, b) => {
            if (a === 'Estrenos') return -1; // 'Estrenos' primero
            if (b === 'Estrenos') return 1; // 'Estrenos' primero
            return 0;
        });
    
        categoriasOrdenadas.forEach(categoria => {
            const categoriaDiv = document.createElement('div');
            categoriaDiv.classList.add('categoria');
            categoriaDiv.innerHTML = `<h3>${categoria}</h3>`;
    
            const categoriaContainer = document.createElement('div');
            categoriaContainer.classList.add('categoria-container');
    
            // Ordenar los animes al revés (de más reciente a más antiguo)
            animesPorCategoria[categoria].reverse().forEach(anime => {
                const animeCard = `
                    <div class="item-anime" data-tmdb-id="${anime.id_tmdb}">
                        <img src="${anime.url_imagen}" alt="${anime.titulo}">
                        <h3>${anime.titulo}</h3>
                    </div>
                `;
                categoriaContainer.insertAdjacentHTML('beforeend', animeCard);
            });
    
            categoriaDiv.appendChild(categoriaContainer);
            animesSection.appendChild(categoriaDiv);
        });
    
        // Event listener para cada anime
        document.querySelectorAll('.item-anime').forEach(item => {
            item.addEventListener('click', function() {
                const tmdbId = this.getAttribute('data-tmdb-id');
                localStorage.setItem('tmdbId
