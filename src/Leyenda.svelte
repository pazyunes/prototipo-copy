<script>
    let leyenda = [
      {
        svg: `
          <svg width="40" height="50" viewBox="0 0 56 70" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="28" cy="6.44737" rx="28" ry="6.44737" fill="#D7B969"/>
            <ellipse cx="28" cy="20.2632" rx="28" ry="20.2632" fill="#D7B969"/>
            <rect x="6" y="23.9474" width="44" height="46.0526" rx="3" fill="#D7B969"/>
          </svg>
        `,
        texto: ": Consumo per capita entre 2.4 kg y 4.2 kg"
      },
      {
        svg: `
          <svg width="47" height="51" viewBox="0 0 125 134" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="62.5" cy="12.3421" rx="62.5" ry="12.3421" fill="#D7B969"/>
            <rect x="14.0977" y="12.3422" width="95.8647" height="121.658" rx="3" fill="#D7B969"/>
          </svg>
        `,
        texto: ": Consumo per capita entre 5.4 kg y 7.1 kg"
      },
      {
        svg: `
          <svg width="52" height="82" viewBox="0 0 175 236" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M87.5 236L0.464447 0.5H174.536L87.5 236Z" fill="#D7B969"/>
          </svg>
        `,
        texto: ": Consumo per capita entre 7.7 kg y 9.8 kg"
      }
    ];
  </script>

<div class="leyenda">
    {#each leyenda as item}
      <div class="leyenda-item">
        {@html item.svg}
        <span>{item.texto}</span>
      </div>
    {/each}
  </div>


  <style>
    .leyenda {
      display: flex;
      justify-content: center;
      flex-direction: row;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 22px;
      width: 100%;
      margin-bottom: 70px;
      padding: 6px;
    }
  
    .leyenda-item {
      display: flex;
      flex-direction: row;
      align-items: center;
      text-align: center;
      width: 420px;
    }
  
    .leyenda-item span {
      margin-top: 8px;
      font-size: 20px;
      color: #333;
      flex-grow: 1;
    }
  
   /* .leyenda-item svg {
      max-width: 100%;
      height: auto;
    }*/
  </style>