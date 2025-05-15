
<script>
    import { schemeTableau10 } from 'd3';
  export let title = "";
  export let tabla2 = [];
  export let tabla = [];
  import { scaleLinear } from 'd3-scale';

  // Escalas dinámicas
  const escalaWidth = scaleLinear().domain([2.4, 9.8]).range([56, 201]);
  const escalaHeight = scaleLinear().domain([2.4, 9.8]).range([63, 426]);
  const escalaOpacity = scaleLinear().domain([2.4, 9.8]).range([0.14, 1]);
  const escalaTranslateY = scaleLinear()
  .domain([2.4, 3.3, 4.2, 5.4, 6.3, 7.1, 7.7, 8.7, 9.2, 9.8])  
  .range([2, -15, -32, -59, -75, -92, -126, -140, -152, -166]);
  const color = scaleLinear().domain([2.4, 9.8]).range(["white", "#69B9FF"]);
  const color2 = scaleLinear().domain([2.3, 5.6]).range(["white", "#DE5D5D"]);
  const escalaTranslateY2 = scaleLinear()
  .domain([2.3, 2.5, 2.8, 3.2, 3.5, 3.8, 4.3, 4.5, 5.0, 5.6])  
  .range([44, 6, -8, -33, -32, -66, -100, -112, -132, -144]);


  </script>  

<h3 class="headline">{title}</h3>
<div class="helados-container">
    {#each tabla as n}
    <div
      class="helado-wrapper"
      style="
        transform: translateY({escalaTranslateY(n.artesanal)}px);
      "
    >
    {#if 2.4<=n.artesanal && n.artesanal <=9.8}
      {#if n.artesanal == 2.4}
    <div class="valor">{n.artesanal}</div>
      <svg width="56" height="63" viewBox="0 0 56 63" fill="none" xmlns="http://www.w3.org/2000/svg">
        <ellipse cx="28" cy="20" rx="28" ry="20" fill="{color(n.artesanal)}"/>
        <ellipse cx="28" cy="28.5" rx="28" ry="3.5" fill="#D7B969"/>
        <ellipse cx="28" cy="36" rx="28" ry="11" fill="#D7B969"/>
        <rect x="6" y="38" width="44" height="25" rx="3" fill="#D7B969"/>
      </svg>   
      <div class="anio">{n.anio}</div>
      {/if}

      {#if n.artesanal == 3.3}
      <div class="valor">{n.artesanal}</div>
      <svg width="56" height="97" viewBox="0 0 56 97" fill="none" xmlns="http://www.w3.org/2000/svg">
        <ellipse cx="28" cy="20" rx="28" ry="20" fill="{color(n.artesanal)}"/>
        <ellipse cx="28" cy="33.4474" rx="28" ry="6.44737" fill="#D7B969"/>
        <ellipse cx="28" cy="47.2632" rx="28" ry="20.2632" fill="#D7B969"/>
        <rect x="6" y="50.9474" width="44" height="46.0526" rx="3" fill="#D7B969"/>
        </svg>
        <div class="anio">{n.anio}</div>
        {/if} 
      {#if n.artesanal == 4.2} 
      <div class="valor">{n.artesanal}</div>
      <svg width="56" height="131" viewBox="0 0 56 131" fill="none" xmlns="http://www.w3.org/2000/svg">
        <ellipse cx="28" cy="20.4688" rx="28" ry="20.4688" fill="{color(n.artesanal)}"/>
        <ellipse cx="28" cy="36.2243" rx="28" ry="9.61493" fill="#D7B969"/>
        <ellipse cx="28" cy="56.8277" rx="28" ry="30.2183" fill="#D7B969"/>
        <rect x="6" y="62.322" width="44" height="68.678" rx="3" fill="#D7B969"/>
        </svg>
        <div class="anio">{n.anio}</div>
        {/if}
        {#if n.artesanal == 5.4}
        <div class="valor">{n.artesanal}</div>
        <svg width="125" height="183" viewBox="0 0 125 183" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="62" cy="40.5" rx="57" ry="40.5" fill="{color(n.artesanal)}"/>
            <ellipse cx="62.5" cy="61.3421" rx="62.5" ry="12.3421" fill="#D7B969"/>
            <rect x="14.0977" y="61.3422" width="95.8647" height="121.658" rx="3" fill="#D7B969"/>
            </svg>
            <div class="anio">{n.anio}</div>
        {/if}
        {#if n.artesanal == 6.3}
        <div class="valor">{n.artesanal}</div>
        <svg width="125" height="217" viewBox="0 0 125 217" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="62" cy="40.6875" rx="57" ry="40.6875" fill="{color(n.artesanal)}"/>
            <ellipse cx="62.5" cy="65.5917" rx="62.5" ry="15.3603" fill="#D7B969"/>
            <rect x="14.0977" y="65.5918" width="95.8647" height="151.408" rx="3" fill="#D7B969"/>
            </svg>
            <div class="anio">{n.anio}</div>
        {/if}
        {#if n.artesanal == 7.1}
        <div class="valor">{n.artesanal}</div>
        <svg width="125" height="251" viewBox="0 0 125 251" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="63" cy="41.1559" rx="57" ry="41.1559" fill="{color(n.artesanal)}"/>
            <ellipse cx="62.5" cy="68.3258" rx="62.5" ry="18.5322" fill="#D7B969"/>
            <rect x="14.0977" y="68.3258" width="95.8647" height="182.674" rx="3" fill="#D7B969"/>
            </svg>
            <div class="anio">{n.anio}</div>
        {/if}
        {#if n.artesanal == 7.7}
        <div class="valor">{n.artesanal}</div>
        <svg width="201" height="324" viewBox="0 0 201 324" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="99.7785" cy="62.9715" rx="87.7785" ry="62.9715" fill="{color(n.artesanal)}"/>
            <path d="M100.5 324L13.4644 88.5H187.536L100.5 324Z" fill="#D7B969"/>
            </svg>
            <div class="anio">{n.anio}</div>
        {/if}
        {#if n.artesanal == 8.7}
        <div class="valor">{n.artesanal}</div>
        <svg width="201" height="358" viewBox="0 0 201 358" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="100.778" cy="65.1555" rx="87.7785" ry="65.1555" fill="{color(n.artesanal)}"/>
            <path d="M100.5 358L13.4644 89.5H187.536L100.5 358Z" fill="#D7B969"/>
            </svg>
            <div class="anio">{n.anio}</div>
        {/if}
        {#if n.artesanal == 9.2}
        <div class="valor">{n.artesanal}</div>
        <svg width="201" height="392" viewBox="0 0 201 392" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="100.778" cy="70.489" rx="87.7785" ry="65.3038" fill="{color(n.artesanal)}"/>
            <path d="M100.5 392L13.4644 98H187.536L100.5 392Z" fill="#D7B969"/>
            </svg>
            <div class="anio">{n.anio}</div>
        {/if}
        {#if n.artesanal == 9.8}
        <div class="valor">{n.artesanal}</div>
        <svg width="201" height="426" viewBox="0 0 201 426" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="100.778" cy="77.8972" rx="87.7785" ry="65.4289" fill="{color(n.artesanal)}"/>
            <path d="M100.5 426L13.4644 106.5H187.536L100.5 426Z" fill="#D7B969"/>
            </svg>
            <div class="anio">{n.anio}</div>
        {/if}                                                            
    {/if}
    </div>
  {/each}


{#each tabla2 as k}
    <div
      class="helado-wrapper"
      style="
        transform: translateY({escalaTranslateY2(k.industrial)}px);
      "
    >
        {#if 2.3 <= k.industrial && k.industrial <= 5.6}
            {#if k.industrial == 2.3}
            <div class="valor">{k.industrial}</div>
            <svg width="56" height="63" viewBox="0 0 56 63" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="28" cy="20" rx="28" ry="20" fill="{color2(k.industrial)}"/>
                <ellipse cx="28" cy="28.5" rx="28" ry="3.5" fill="#D7B969"/>
                <ellipse cx="28" cy="36" rx="28" ry="11" fill="#D7B969"/>
                <rect x="6" y="38" width="44" height="25" rx="3" fill="#D7B969"/>
                </svg>   
            <div class="anio">{k.anio}</div>
            {/if}
            {#if k.industrial == 3.5}
            <div class="valor">{k.industrial}</div>
            <svg width="125" height="217" viewBox="0 0 125 217" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="62" cy="40.6875" rx="57" ry="40.6875" fill="{color2(k.industrial)}"/>
                <ellipse cx="62.5" cy="65.5917" rx="62.5" ry="15.3603" fill="#D7B969"/>
                <rect x="14.0977" y="65.5918" width="95.8647" height="151.408" rx="3" fill="#D7B969"/>
                </svg>
                <div class="anio">{k.anio}</div>
            {/if}
            {#if k.industrial == 4.5}
            <div class="valor">{k.industrial}</div>
            <svg width="201" height="358" viewBox="0 0 201 358" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="100.778" cy="65.1555" rx="87.7785" ry="65.1555" fill="{color2(k.industrial)}"/>
                <path d="M100.5 358L13.4644 89.5H187.536L100.5 358Z" fill="#D7B969"/>
                </svg>
                <div class="anio">{k.anio}</div>
            {/if}
            {#if k.industrial == 5.6}
            <div class="valor">{k.industrial}</div>
            <svg width="201" height="426" viewBox="0 0 201 426" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="100.778" cy="77.8972" rx="87.7785" ry="65.4289" fill="{color2(k.industrial)}"/>
                <path d="M100.5 426L13.4644 106.5H187.536L100.5 426Z" fill="#D7B969"/>
                </svg>
                <div class="anio">{k.anio}</div>
            {/if}
            {#if k.industrial == 5.0}
            <div class="valor">{k.industrial}</div>
            <svg width="201" height="392" viewBox="0 0 201 392" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="100.778" cy="70.489" rx="87.7785" ry="65.3038" fill="{color2(k.industrial)}"/>
                <path d="M100.5 392L13.4644 98H187.536L100.5 392Z" fill="#D7B969"/>
                </svg>
                <div class="anio">{k.anio}</div>
            {/if}
            {#if k.industrial == 4.3}
            <div class="valor">{k.industrial}</div>
            <svg width="201" height="324" viewBox="0 0 201 324" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="99.7785" cy="62.9715" rx="87.7785" ry="62.9715" fill="{color2(k.industrial)}"/>
                <path d="M100.5 324L13.4644 88.5H187.536L100.5 324Z" fill="#D7B969"/>
                </svg>
                <div class="anio">{k.anio}</div>
            {/if}
            {#if k.industrial == 3.8}
            <div class="valor">{k.industrial}</div>
            <svg width="125" height="251" viewBox="0 0 125 251" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="63" cy="41.1559" rx="57" ry="41.1559" fill="{color2(k.industrial)}"/>
                <ellipse cx="62.5" cy="68.3258" rx="62.5" ry="18.5322" fill="#D7B969"/>
                <rect x="14.0977" y="68.3258" width="95.8647" height="182.674" rx="3" fill="#D7B969"/>
                </svg>
                <div class="anio">{k.anio}</div>
            {/if}
            {#if k.industrial == 3.2}
            <div class="valor">{k.industrial}</div>
            <svg width="125" height="183" viewBox="0 0 125 183" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="62" cy="40.5" rx="57" ry="40.5" fill="{color2(k.industrial)}"/>
                <ellipse cx="62.5" cy="61.3421" rx="62.5" ry="12.3421" fill="#D7B969"/>
                <rect x="14.0977" y="61.3422" width="95.8647" height="121.658" rx="3" fill="#D7B969"/>
                </svg>
                <div class="anio">{k.anio}</div>
            {/if}
            {#if k.industrial == 2.8}
            <div class="valor">{k.industrial}</div>
            <svg width="56" height="131" viewBox="0 0 56 131" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="28" cy="20.4688" rx="28" ry="20.4688" fill="{color2(k.industrial)}"/>
                <ellipse cx="28" cy="36.2243" rx="28" ry="9.61493" fill="#D7B969"/>
                <ellipse cx="28" cy="56.8277" rx="28" ry="30.2183" fill="#D7B969"/>
                <rect x="6" y="62.322" width="44" height="68.678" rx="3" fill="#D7B969"/>
                </svg>
                <div class="anio">{k.anio}</div>
            {/if}
            {#if k.industrial == 2.5}
            <div class="valor">{k.industrial}</div>
            <svg width="56" height="97" viewBox="0 0 56 97" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="28" cy="20" rx="28" ry="20" fill="{color2(k.industrial)}"/>
                <ellipse cx="28" cy="33.4474" rx="28" ry="6.44737" fill="#D7B969"/>
                <ellipse cx="28" cy="47.2632" rx="28" ry="20.2632" fill="#D7B969"/>
                <rect x="6" y="50.9474" width="44" height="46.0526" rx="3" fill="#D7B969"/>
                </svg>
                <div class="anio">{k.anio}</div>
            {/if}

        {/if}
    </div>
{/each}
</div> 


<style>
    .helados-container {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 40px;
    }
    .helado-wrapper {
      position: relative;
      width: auto;
      height: auto;
      text-align: center;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 15px;
      margin-bottom: 10px;
    }  
    .valor {
    margin-bottom: 4px;
    font-size: 20px;
    font-weight: bold;
  }

  .anio {
    margin-top: 4px;
    font-size: 20px;
    font-weight: bold;
  }
</style>
    