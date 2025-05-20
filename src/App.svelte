<!-- Script JS -->
<script>
  /* Importamos d3 para tenerlo disponible */
  import * as d3 from 'd3'
  import Helado from './Helado.svelte';
  import Leyenda from './Leyenda.svelte';
  let numbers = [24, 33, 42, 54, 63, 71, 77, 87, 92, 98];
  let numbers2 = [23, 35, 45, 56, 50, 43, 38, 32, 28, 25];
  let tabla = [
    {anio: 2015, artesanal: 2.4}, 
    {anio: 2016, artesanal: 3.3}, 
    {anio: 2017, artesanal: 4.2}, 
    {anio: 2018, artesanal: 5.4}, 
    {anio: 2019, artesanal: 6.3}, 
    {anio: 2020, artesanal: 7.1}, 
    {anio: 2021, artesanal: 7.7}, 
    {anio: 2022, artesanal: 8.7}, 
    {anio: 2023, artesanal: 9.2}, 
    {anio: 2024, artesanal: 9.8}, 
  ];
  let tabla2 = [
    {anio: 2015, industrial: 2.3}, 
    {anio: 2016, industrial: 3.5}, 
    {anio: 2017, industrial: 4.5}, 
    {anio: 2018, industrial: 5.6}, 
    {anio: 2019, industrial: 5.0}, 
    {anio: 2020, industrial: 4.3}, 
    {anio: 2021, industrial: 3.8}, 
    {anio: 2022, industrial: 3.2}, 
    {anio: 2023, industrial: 2.8}, 
    {anio: 2024, industrial: 2.5} ];

</script>

<!-- Estructura contenido HTML -->

<div class="noticia-header">
  <span class="categoria">Tendencias</span>
  <span class="fecha">30 de abril de 2025</span>
</div>

<main id="container">
  <div class="header-container">
  <h1 class="title">Consumo del helado artesanal vs. industrial</h1>
  <h2 class="subtitle">El contraste en sus tendencias</h2>
  </div>
  
  <div class= "tamaños-container"> 
  <div class="text-box">
    <p>Durante los últimos años, el consumo de helado mostró una transformación significativa, marcada por 
      la evolución de dos grandes categorías: el helado artesanal y el helado industrial. Aunque ambos coexisten 
      en el mercado, sus trayectorias recientes reflejan diferencias notables en tendencias y preferencias del público.</p>
  </div>
  </div>

  <div class= "tamaños-container">
    <div class="titulo-helados">
      <p> El helado <span style = "color: #69B9FF">artesanal</span> conquista el paladar y el mercado </p>
    </div>
    <div class="mini-titulo"><p>Consumo per capita</p></div>
    <Leyenda />
    <div class="page-center"> 
    <div class = "helados-wrapper">
      <Helado tabla={tabla} />
    </div>
  </div>
    <div class = "text-box"> 
      <p> <b>El crecimiento del helado artesanal, visualizado en cada cucurucho</b> </p>
      <p>A través de helados que aumentan progresivamente en tamaño y opacidad, este gráfico ilustra de forma visual y atractiva 
      el crecimiento sostenido del consumo per cápita de helado artesanal en los últimos años. La elección de cucuruchos más grandes 
      y nítidos representa cómo esta categoría fue ganando protagonismo en la preferencia de los consumidores, marcando una tendencia 
      que combina calidad, tradición y disfrute. </p>
    </div>

    <div class="titulo-helados">
      <p> Helado <span style="color: #DE5D5D">industrial</span>: éxito fugaz, caída inevitable </p>
    </div>
    <div class="mini-titulo"><p>Consumo per capita</p></div>
    <Leyenda />
    <div class = "page-center">
    <div class = "helados-wrapper">
      <Helado tabla2={tabla2} />
    </div>
  </div>
    <div class = "text-box"> 
      <p>  <b>Un consumo que tocó su techo y luego descendió </b> </p>
      <p>El gráfico representa el consumo per cápita de helado industrial desde 2015 hasta 2024. Se observa un crecimiento 
        constante hasta alcanzar su punto máximo alrededor de 2019, seguido de una caída progresiva en los años posteriores. Esto 
        podría vincularse a cambios en las preferencias del consumidor, una mayor valorización del helado artesanal, o factores 
        económicos que afectaron el mercado de productos industrializados. </p>
    </div>

    <hr />
  </div>

  <div class = "grafico-container">
    <h2 class="subtitle"> A partir del 2018 el helado <span style = "color: #69B9FF">artesanal</span> comienza a superar al <span style="color: #DE5D5D">industrial</span> </h2>
    <div class = "graficos">
      <iframe
      src="https://flo.uri.sh/story/3098431/embed"
      frameborder="0"
      scrolling="no"
      title="Gráfico interactivo de Flourish2"
      class="flourish-iframe"
   
    ></iframe>    
    </div>
    <div class = "text-box">
      <p> El gráfico evidencia una clara divergencia en las trayectorias de consumo entre el helado artesanal y el industrial 
        en el período 2015–2024. </p>
      <p> Mientras el consumo per cápita de helado artesanal muestra un crecimiento sostenido, con una pendiente positiva constante, 
        el helado industrial presenta un punto de inflexión en 2019, a partir del cual comienza un descenso progresivo. </p>
      <p> Este cambio sugiere una reconfiguración en las preferencias del consumidor, que pasan a valorar más los productos artesanales, 
        asociados a la calidad, el disfrute y la tradición, en detrimento de las opciones industrializadas. El cruce de las curvas en 
        2018-2019 marca el momento en que el consumo artesanal supera por primera vez al industrial, consolidando una tendencia que se 
        mantendrá en ascenso hacia 2024. </p>
    </div>
  </div>

  <div class = "grafico-container">
    <h2 class="subtitle"> La brecha se amplía: el consumo <span style = "color: #69B9FF">artesanal</span> lidera con fuerza </h2>
      <div class = "graficos">
        <iframe
        src="https://flo.uri.sh/story/3098462/embed"
        frameborder="0"
        scrolling="no"
        title="Gráfico interactivo de Flourish2"
        class="flourish-iframe"
     
      ></iframe>    
      </div>
    <div class = "text-box">
      <p> Este gráfico muestra la diferencia anual en el consumo per cápita de helado artesanal frente al industrial entre 2015 y 2024. </p>
      <p> Se observa que, hasta 2018, el consumo industrial superaba ligeramente al artesanal, con diferencias negativas.
        Sin embargo, a partir de 2019 se produce un punto de inflexión, y desde ese año el consumo artesanal no solo lo supera, 
        sino que la brecha se amplía año tras año. </p>
      <p> La visualización resalta claramente esta transformación en las preferencias del consumidor: mientras el helado industrial 
        pierde protagonismo, el artesanal crece de forma sostenida, consolidando una tendencia de cambio hacia opciones más valoradas 
        por su calidad y tradición. </p>
    </div>
  </div>

  <div class="sabias-que">
    <h4>¿Sabías que…?</h4>
    <ul>
      <li>Entre 2015 y 2024, el consumo de helado artesanal creció más del 100%, reflejando un fuerte cambio en las preferencias del público.</li>
      <li>En 2024, se consumen casi 4 kilos más de helado artesanal que industrial, marcando una clara diferencia entre ambas categorías.</li>
      <li>Esta tendencia está liderada por los jóvenes, que prefieren productos más artesanales y de mayor calidad.</li>
    </ul>
  </div>

</main>


<footer class="footer">
  <p>&copy; 2025 Maria Paz Yunes</p>
  <p>Contacto: <a href="mailto:myunesmarangoni@mail.utdt.edu">myunesmarangoni@mail.utdt.edu</a></p>
  
  <div class="footer-links">
    <a href="https://github.com/pazyunes" target="_blank">
      <img src="./images/github.png" alt="GitHub" class="icono-footer">
    </a>
    |
    <a href="https://www.utdt.edu/" target="_blank">
      <img src="./images/UTDT.JPG" alt="UTDT" class="icono-footer">
    </a>
  </div>
</footer>

<!-- Estilos CSS -->
<style>
  :global(body) {
    font-family: 'Merriweather' , serif;
    height: auto;
    background-color: #f8f9fa;
    overflow-x: hidden;
  }

  #container {
    width: 100%;
    padding: 0;
    margin: 0;
  }
  
  .title {
    font-size: 55px; 
    font-weight: bold; 
    text-align: center; 
    color: black; 
    margin-bottom: 10px; 
    margin-top: 20px;
  }

  .subtitle {
    font-size: 32px; 
    font-weight: 800; 
    text-align: center;
    color: black; 
    margin-bottom: 20px; 
  }

  .titulo-helados {
    font-size: 32px; 
    font-weight: bold; 
    text-align: center;
    color: black; 
    margin-bottom: 0px; 
  }

  .text-box{
    text-align: left;
    text-wrap: flex;
    font-size: 25px;
    max-width: 900px;
    padding: 10px;
    margin-bottom: 20px;
  }

  .mini-titulo{
    text-align: left;
    text-wrap: flex;
    font-size: 22px;
    max-width: 1300px;
    padding: 10px;
    margin-top: 5px;

  }

  .tamaños-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: auto;    
    margin-top: 20px;
    padding: 0;
    margin-bottom: 10px;
    width: auto;
  }

  .page-center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 65vh; /* ocupa todo el alto de la pantalla */
  width: 100vw;  /* ocupa todo el ancho */
}
  .grafico-container {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    height: auto;  
    border-radius: 10px; 
    width: auto;  
    margin-top: 30px;
    padding: 0;
  }

  .helados-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-grow: 1; 
    flex: 1 1 auto;
    width: auto;
    margin-top: 50px;
    margin-bottom: 2px;
  }

  .noticia-header {
    display: flex;
    justify-content: space-between;
    font-size: 30px;
    background-color: #f2f2f2;
    padding: 10px;
    color: #555;
    margin-bottom: auto;
    border-bottom: 1px solid #ccc;
    height: 10vh;
    align-items: center;
    box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    width: auto;
  }

  .categoria {
    font-weight: bold;
    color: black;
  }

  .footer {
    background-color: #f2f2f2;
    padding: 10px;
    text-align: center;
    align-items: center;
    font-size: 0.9rem;
    color: #555;
    margin-top: auto;
    margin-bottom: auto;
    border-top: 1px solid #ccc;
    font-size: 20px;
  }

  .graficos {
    width: 80%;
    display: flex;
    justify-content: center;
    height: 70vh;
  }

  .graficos iframe{
    width:70%;
    height: 100%;
  }


    .sabias-que {
    background-color: #fff4f4;
    border-left: 5px solid #f08080;
    padding: 20px 25px;
    margin: 40px auto;
    border-radius: 8px;
    color: #000000;
    box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    font-size: 24px;
    max-width: 1200px;
  }

  .sabias-que h4 {
    color: #cc4b4b;
    font-size: 30px;
    margin-bottom: 12px;
  }

  .sabias-que ul {
    list-style-type: disc;
    padding-left: 20px;
    margin: 0;
  }

  .sabias-que li {
    margin-bottom: 8px;
    line-height: 1.6;
  }

  .icono-footer {
    width: 40px;   
    height: auto;  
    margin: 0 8px; 
    vertical-align: middle; 
  }


</style>
