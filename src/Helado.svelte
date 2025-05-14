
<script>
    import { schemeTableau10 } from 'd3';
  export let title = "";
  export let numbers = [];
  export let numbers2 = [];
  import { scaleLinear } from 'd3-scale';
  //export let tabla = [];

  // Escalas dinámicas
  const escalaWidth = scaleLinear().domain([24, 98]).range([56, 201]);
  const escalaHeight = scaleLinear().domain([24, 98]).range([63, 426]);
  const escalaOpacity = scaleLinear().domain([24, 98]).range([0.14, 1]);
  const escalaTranslateY = scaleLinear()
  .domain([24, 33, 42, 54, 63, 71, 77, 87, 92, 98])  
  .range([2, -15, -32, -59, -75, -92, -126, -140, -152, -166]);
  const color = scaleLinear().domain([24, 98]).range(["white", "#E36567"]);
  const escalaTranslateY2 = scaleLinear()
  .domain([23, 25, 28, 32, 35, 38, 43, 45, 50, 56])  
  .range([44, 6, -8, -33, -32, -66, -100, -112, -132, -144]);
  </script>  

<h3 class="headline">{title}</h3>
<div class="helados-container">
    {#each numbers as n}
    <div
      class="helado-wrapper"
      style="
        transform: translateY({escalaTranslateY(n)}px);
      "
    >
    {#if 24<=n && n <=98}
      {#if n == 24}
      <svg width="56" height="63" viewBox="0 0 56 63" fill="none" xmlns="http://www.w3.org/2000/svg">
        <ellipse cx="28" cy="20" rx="28" ry="20" fill="{color(n)}"/>
        <ellipse cx="28" cy="28.5" rx="28" ry="3.5" fill="#D7B969"/>
        <ellipse cx="28" cy="36" rx="28" ry="11" fill="#D7B969"/>
        <rect x="6" y="38" width="44" height="25" rx="3" fill="#D7B969"/>
        </svg>   
      {/if}

      {#if n == 33}
      <svg width="56" height="97" viewBox="0 0 56 97" fill="none" xmlns="http://www.w3.org/2000/svg">
        <ellipse cx="28" cy="20" rx="28" ry="20" fill="{color(n)}"/>
        <ellipse cx="28" cy="33.4474" rx="28" ry="6.44737" fill="#D7B969"/>
        <ellipse cx="28" cy="47.2632" rx="28" ry="20.2632" fill="#D7B969"/>
        <rect x="6" y="50.9474" width="44" height="46.0526" rx="3" fill="#D7B969"/>
        </svg>
        {/if} 
      {#if n == 42}  
      <svg width="56" height="131" viewBox="0 0 56 131" fill="none" xmlns="http://www.w3.org/2000/svg">
        <ellipse cx="28" cy="20.4688" rx="28" ry="20.4688" fill="{color(n)}"/>
        <ellipse cx="28" cy="36.2243" rx="28" ry="9.61493" fill="#D7B969"/>
        <ellipse cx="28" cy="56.8277" rx="28" ry="30.2183" fill="#D7B969"/>
        <rect x="6" y="62.322" width="44" height="68.678" rx="3" fill="#D7B969"/>
        </svg>
        {/if}
        {#if n == 54}
        <svg width="125" height="183" viewBox="0 0 125 183" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="62" cy="40.5" rx="57" ry="40.5" fill="{color(n)}"/>
            <ellipse cx="62.5" cy="61.3421" rx="62.5" ry="12.3421" fill="#D7B969"/>
            <rect x="14.0977" y="61.3422" width="95.8647" height="121.658" rx="3" fill="#D7B969"/>
            </svg>
        {/if}
        {#if n == 63}
        <svg width="125" height="217" viewBox="0 0 125 217" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="62" cy="40.6875" rx="57" ry="40.6875" fill="{color(n)}"/>
            <ellipse cx="62.5" cy="65.5917" rx="62.5" ry="15.3603" fill="#D7B969"/>
            <rect x="14.0977" y="65.5918" width="95.8647" height="151.408" rx="3" fill="#D7B969"/>
            </svg>
        {/if}
        {#if n == 71}
        <svg width="125" height="251" viewBox="0 0 125 251" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="63" cy="41.1559" rx="57" ry="41.1559" fill="{color(n)}"/>
            <ellipse cx="62.5" cy="68.3258" rx="62.5" ry="18.5322" fill="#D7B969"/>
            <rect x="14.0977" y="68.3258" width="95.8647" height="182.674" rx="3" fill="#D7B969"/>
            </svg>
        {/if}
        {#if n == 77}
        <svg width="201" height="324" viewBox="0 0 201 324" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="99.7785" cy="62.9715" rx="87.7785" ry="62.9715" fill="{color(n)}"/>
            <path d="M100.5 324L13.4644 88.5H187.536L100.5 324Z" fill="#D7B969"/>
            </svg>
        {/if}
        {#if n == 87}
        <svg width="201" height="358" viewBox="0 0 201 358" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="100.778" cy="65.1555" rx="87.7785" ry="65.1555" fill="{color(n)}"/>
            <path d="M100.5 358L13.4644 89.5H187.536L100.5 358Z" fill="#D7B969"/>
            </svg>
        {/if}
        {#if n == 92}
        <svg width="201" height="392" viewBox="0 0 201 392" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="100.778" cy="70.489" rx="87.7785" ry="65.3038" fill="{color(n)}"/>
            <path d="M100.5 392L13.4644 98H187.536L100.5 392Z" fill="#D7B969"/>
            </svg>
        {/if}
        {#if n == 98}
        <svg width="201" height="426" viewBox="0 0 201 426" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="100.778" cy="77.8972" rx="87.7785" ry="65.4289" fill="{color(n)}"/>
            <path d="M100.5 426L13.4644 106.5H187.536L100.5 426Z" fill="#D7B969"/>
            </svg>
        {/if}                                                            
    {/if}
    </div>
  {/each}


{#each numbers2 as k}
    <div
      class="helado-wrapper"
      style="
        transform: translateY({escalaTranslateY2(k)}px);
      "
    >
        {#if 23 <= k && k <= 56}
            {#if k == 23}
            <svg width="56" height="63" viewBox="0 0 56 63" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="28" cy="20" rx="28" ry="20" fill="{color(k)}"/>
                <ellipse cx="28" cy="28.5" rx="28" ry="3.5" fill="#D7B969"/>
                <ellipse cx="28" cy="36" rx="28" ry="11" fill="#D7B969"/>
                <rect x="6" y="38" width="44" height="25" rx="3" fill="#D7B969"/>
                </svg>   
            {/if}
            {#if k == 35}
            <svg width="125" height="217" viewBox="0 0 125 217" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="62" cy="40.6875" rx="57" ry="40.6875" fill="{color(k)}"/>
                <ellipse cx="62.5" cy="65.5917" rx="62.5" ry="15.3603" fill="#D7B969"/>
                <rect x="14.0977" y="65.5918" width="95.8647" height="151.408" rx="3" fill="#D7B969"/>
                </svg>
            {/if}
            {#if k == 45}
            <svg width="201" height="358" viewBox="0 0 201 358" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="100.778" cy="65.1555" rx="87.7785" ry="65.1555" fill="{color(k)}"/>
                <path d="M100.5 358L13.4644 89.5H187.536L100.5 358Z" fill="#D7B969"/>
                </svg>
            {/if}
            {#if k == 56}
            <svg width="201" height="426" viewBox="0 0 201 426" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="100.778" cy="77.8972" rx="87.7785" ry="65.4289" fill="{color(k)}"/>
                <path d="M100.5 426L13.4644 106.5H187.536L100.5 426Z" fill="#D7B969"/>
                </svg>
            {/if}
            {#if k == 50}
            <svg width="201" height="392" viewBox="0 0 201 392" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="100.778" cy="70.489" rx="87.7785" ry="65.3038" fill="{color(k)}"/>
                <path d="M100.5 392L13.4644 98H187.536L100.5 392Z" fill="#D7B969"/>
                </svg>
            {/if}
            {#if k == 43}
            <svg width="201" height="324" viewBox="0 0 201 324" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="99.7785" cy="62.9715" rx="87.7785" ry="62.9715" fill="{color(k)}"/>
                <path d="M100.5 324L13.4644 88.5H187.536L100.5 324Z" fill="#D7B969"/>
                </svg>
            {/if}
            {#if k == 38}
            <svg width="125" height="251" viewBox="0 0 125 251" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="63" cy="41.1559" rx="57" ry="41.1559" fill="{color(k)}"/>
                <ellipse cx="62.5" cy="68.3258" rx="62.5" ry="18.5322" fill="#D7B969"/>
                <rect x="14.0977" y="68.3258" width="95.8647" height="182.674" rx="3" fill="#D7B969"/>
                </svg>
            {/if}
            {#if k == 32}
            <svg width="125" height="183" viewBox="0 0 125 183" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="62" cy="40.5" rx="57" ry="40.5" fill="{color(k)}"/>
                <ellipse cx="62.5" cy="61.3421" rx="62.5" ry="12.3421" fill="#D7B969"/>
                <rect x="14.0977" y="61.3422" width="95.8647" height="121.658" rx="3" fill="#D7B969"/>
                </svg>
            {/if}
            {#if k == 28}
            <svg width="56" height="131" viewBox="0 0 56 131" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="28" cy="20.4688" rx="28" ry="20.4688" fill="{color(k)}"/>
                <ellipse cx="28" cy="36.2243" rx="28" ry="9.61493" fill="#D7B969"/>
                <ellipse cx="28" cy="56.8277" rx="28" ry="30.2183" fill="#D7B969"/>
                <rect x="6" y="62.322" width="44" height="68.678" rx="3" fill="#D7B969"/>
                </svg>
            {/if}
            {#if k == 25}
            <svg width="56" height="97" viewBox="0 0 56 97" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="28" cy="20" rx="28" ry="20" fill="{color(k)}"/>
                <ellipse cx="28" cy="33.4474" rx="28" ry="6.44737" fill="#D7B969"/>
                <ellipse cx="28" cy="47.2632" rx="28" ry="20.2632" fill="#D7B969"/>
                <rect x="6" y="50.9474" width="44" height="46.0526" rx="3" fill="#D7B969"/>
                </svg>
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
      align-items: center;
      justify-content: center;
      padding: 15px;
      margin-bottom: 10px;
    }  
</style>
    