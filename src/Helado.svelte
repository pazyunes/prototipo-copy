
<script>
  export let title = "";
  export let numbers = [];
  export let tabla = [];
  export let numbers2 = [];
  export let tabla2 = [];
  import { scaleLinear } from 'd3-scale';

  // Escalas dinámicas
  const escalaWidth = scaleLinear().domain([24, 98]).range([32, 104.5]);
  const escalaHeight = scaleLinear().domain([24, 98]).range([36.5, 228]);
  const escalaOpacity = scaleLinear().domain([24, 98]).range([0.14, 1]);
  const escalaTranslateY = scaleLinear()
  .domain([24, 33, 42, 54, 63, 71, 77, 87, 92, 98])  // valores de n
  .range([2, -3, -12, -5, -16, -24, -48, -62, -72, -87]);  // valores top

  // Función para obtener el path de imagen según el número
  function getImageSrc(n) {
    if (0 <= n && n <= 24) return "./images/Group 5.svg";
    if (24 < n && n <= 33) return "./images/Group 4.svg";
    if (33 < n && n <= 42) return "./images/Group 6.svg";
    if (42 < n && n <= 54) return "./images/Group 9.svg";
    if (54 < n && n <= 63) return "./images/Group 8.svg";
    if (63 < n && n <= 71) return "./images/Group 10.svg";
    if (71 < n && n <= 77) return "./images/Group 13.svg";
    if (77 < n && n <= 87) return "./images/Group 12.svg";
    if (87 < n && n <= 92) return "./images/Group 14.svg";
    if (92 < n && n <= 98) return "./images/Group 17.svg";
    return ""; // valor por defecto
  }

  function getImageSrc2(k) {
  if (k === 23) return "./images/Group 5.svg";
  if (k === 25) return "./images/Group 4.svg";
  if (k === 28) return "./images/Group 6.svg";
  if (k === 32) return "./images/Group 9.svg";
  if (k === 35) return "./images/Group 8.svg";
  if (k === 38) return "./images/Group 10.svg";
  if (k === 43) return "./images/Group 13.svg";
  if (k === 45) return "./images/Group 12.svg";
  if (k === 50) return "./images/Group 14.svg";
  if (k === 56) return "./images/Group 17.svg";
  return ""; // en caso de que no esté en la lista
}
</script>  

<h3 class="headline">{title}</h3>
<div class="helados-container">
    {#each numbers as n}
  {#if 24 <= n && n <= 98}
    <div class="helado-wrapper">
      <img 
        src="{getImageSrc(n)}"
        alt="helado-img"
        style="
          width: {escalaWidth(n)}px; 
          height: {escalaHeight(n)}px; 
          opacity: {escalaOpacity(n)};
          transform: translateY({escalaTranslateY(n)}px);
        "
      />
    </div>
  {/if}
{/each}

{#each numbers2 as k}
    <div class="helado-wrapper">
        {#if 23 <= k && k <= 56}
            {#if k == 23}
            <div class="pri"> 
                <img class="small1" src="./images/Group 5.svg" alt="helado-img" />      
            </div>
            {/if}
            {#if k == 35}
            <div class="quin"> 
                <img class="medium2" src="./images/Group 8.svg" alt="helado-img" /> 
            </div>
            {/if}
            {#if k == 45}
            <div class="oct"> 
                <img class="large2" src="./images/Group 12.svg" alt="helado-img" />  
            </div>
            {/if}
            {#if k == 56}
            <div class="dec"> 
                <img class="large4" src="./images/Group 17.svg" alt="helado-img" />  
            </div>
            {/if}
            {#if k == 50}
            <div class="nov"> 
                <img class="large3" src="./images/Group 14.svg" alt="helado-img" /> 
            </div>
            {/if}
            {#if k == 43}
            <div class="sept"> 
                <img class="large1" src="./images/Group 13.svg" alt="helado-img" />  
            </div>
            {/if}
            {#if k == 38}
            <div class="sext"> 
                <img class="medium3" src="./images/Group 10.svg" alt="helado-img" />   
            </div>
            {/if}
            {#if k == 32}
            <div class="cuar"> 
                <img class="medium1" src="./images/Group 9.svg" alt="helado-img" /> 
            </div>
            {/if}
            {#if k == 28}
            <div class="ter"> 
                <img class="small3" src="./images/Group 6.svg" alt="helado-img" /> 
            </div>
            {/if}
            {#if k == 25}
            <div class="seg">  
                <img class="small2" src="./images/Group 4.svg" alt="helado-img" />     
            </div>
            {/if}

        {/if}
    </div>
    {/each}
</div> 



{#if tabla.length > 0}
<table class="tabla">
    <tbody>
        <tr>
            <th class="anio"> Año </th>
            {#each tabla as dato}
            <th class="anio">{dato.anio}</th>
            {/each}
        </tr>
        <tr>
            <td class="consumo"> Consumo per cápita (kg/año)</td>
        {#each tabla as dato}
            <td class="consumo">{dato.consumo}</td>
        {/each}
        </tr>
    <tbody/>
</table>
{/if}

{#if tabla2.length > 0}
<table class="tabla">
    <tbody>
        <tr>
            <th class="anio"> Año </th>
            {#each tabla2 as dato}
            <th class="anio">{dato.anio}</th>
            {/each}
        </tr>
        <tr>
            <td class="consumo"> Consumo per cápita (kg/año)</td>
        {#each tabla2 as dato}
            <td class="consumo">{dato.industrial}</td>
        {/each}
        </tr>
    <tbody/>
</table>
{/if}



<style>
    .helados-container {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 10px;
    }
    .helado-wrapper {
      position: relative;
      width: auto;
      text-align: center;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 15px;
      margin-bottom: 0;
    }

    .pri img {
        width: 32px;
        height: 36.5px;
        opacity: 0.14;
    }

    .seg img {
        width: 32px;
        height: 42.5px;
        position: relative;
        top: -3px;
        opacity: 0.2;
    }

    .ter img {
        width: 32px;
        height: 48px;
        position: relative;
        top: -5px;
        opacity: 0.3;
    }

    .cuar img {
        width: 77.5px;
        height: 66px;
        position: relative;
        top: -14px;
        opacity: 0.4;
    }

    .quin img {
        width: 81.5px;
        height: 82px;
        position: relative;
        top: -21px;
        opacity: 0.5;
    }

    .sext img {
        width: 81.5px;
        height: 93px;
        position: relative;
        top: -26px;
        opacity: 0.6;
    }

    .sept img {
        width: 100.5px;
        height: 161.5px;
        position: relative;
        top: -56px;
        opacity: 0.7;
    }

    .oct img {
        width: 100.5px;
        height: 180.5px;
        position: relative;
        top: -62px;
        opacity: 0.8;
    }

    .nov img {
        width: 100.5px;
        height: 197.5px;
        position: relative;
        top: -72px;
        opacity: 0.9;
    }

    .dec img {
        width: 104.5px;
        height: 228px;
        position: relative;
        top: -87px;
        opacity: 1;
    }  
    .tabla {
        width: auto;
        border-collapse: collapse;
        border-spacing: 20px 0; /* separación horizontal y vertical */
        margin: 20px auto;
        font-family: 'Merriweather', serif;
        text-align: center;
        font-size: 18px;
    }

    .tabla td{
        padding: 35px;
        padding-top: 5px;
    }
    .tabla th {
        text-align: center; /* mantiene centrado */
        padding-left: 10px; /* pero igual lo empuja un poquito */
    }

    .anio {
        border-bottom: 2px solid #333; /* Línea continua debajo de los años */
        padding-bottom: 4px;
    }

    .consumo {
        color: #555;
        font-weight: bold;
    }

</style>
    