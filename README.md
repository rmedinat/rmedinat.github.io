<html lang="es-MX">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>¡Lilian cumple 2!</title>
<meta property="og:title" content="¡Lilian cumple 2 años!">
<meta property="og:description" content="Sábado 3 de octubre · Una fiesta de hadas en el bosque">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@600;700;800&family=Caveat:wght@600;700&family=Grand+Hotel&family=Nunito:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --crema:#FFF8F2;
    --durazno:#FDE7DA;
    --rosa:#E28BA2;
    --rosa-osc:#C4667F;
    --rosa-palo:#F7D6DE;
    --vino:#B04A5A;
    --dorado:#EFC15E;
    --terracota:#DC8A57;
    --salvia:#8A9E72;
    --salvia-osc:#61754C;
    --cafe:#6B4A3A;

    --script:"Grand Hotel", cursive;
    --titulo:"Baloo 2", system-ui, sans-serif;
    --mano:"Caveat", cursive;
    --cuerpo:"Nunito", system-ui, sans-serif;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{-webkit-text-size-adjust:100%}
  body{background:#EBD3D0;color:var(--cafe);font-family:var(--cuerpo);font-weight:400;line-height:1.65}
  .lienzo{
    position:relative;max-width:480px;margin:0 auto;overflow:hidden;
    background-color:var(--crema);
    background-image:
      radial-gradient(circle at 14px 14px, rgba(226,139,162,.13) 3px, transparent 3.1px),
      radial-gradient(circle at 40px 40px, rgba(239,193,94,.14) 2.4px, transparent 2.5px);
    background-size:54px 54px, 54px 54px;
  }
  @media (min-width:520px){
    body{padding:24px 0}
    .lienzo{box-shadow:0 16px 50px rgba(107,74,58,.28);border-radius:26px}
  }
  .sprites{position:absolute;width:0;height:0;overflow:hidden}

  /* pétalos y hojas cayendo */
  .hojas{position:fixed;inset:0;pointer-events:none;z-index:6;overflow:hidden}
  .hoja{position:absolute;top:-12vh;opacity:0;animation:caer linear infinite}
  @keyframes caer{
    0%{transform:translate3d(0,-12vh,0) rotate(0deg);opacity:0}
    8%{opacity:.9}
    50%{transform:translate3d(30px,55vh,0) rotate(200deg)}
    92%{opacity:.75}
    100%{transform:translate3d(-22px,116vh,0) rotate(430deg);opacity:0}
  }

  .guirnalda{display:block;width:100%;height:auto;position:relative;z-index:4}

  /* ---------- portada ---------- */
  .portada{position:relative;padding:4px 22px 186px;text-align:center}
  .portada .cielo{position:absolute;left:0;right:0;bottom:0;height:auto;width:100%;z-index:0}
  .portada .contenido{position:relative;z-index:3;padding-top:4px}

  .saludo{font-family:var(--mano);font-size:29px;line-height:1.1;color:var(--salvia-osc);transform:rotate(-3deg);display:inline-block}

  .nombre-wrap{position:relative;display:inline-block;margin:6px 0 2px;padding:0 30px}
  .nombre{
    font-family:var(--script);font-size:clamp(56px,17vw,76px);line-height:1.15;color:var(--vino);
    text-shadow:0 3px 0 rgba(226,139,162,.35);
  }
  .subrayado{display:block;width:100%;height:auto;margin-top:-6px}

  .insignia{
    position:relative;display:flex;flex-direction:column;align-items:center;justify-content:center;
    width:110px;height:110px;margin:10px auto 4px;
  }
  .insignia .corona{position:absolute;inset:0;width:100%;height:100%}
  .insignia b{position:relative;font-family:var(--titulo);font-weight:800;font-size:44px;line-height:.85;color:var(--vino)}
  .insignia span{position:relative;font-family:var(--mano);font-size:20px;line-height:1;color:var(--rosa-osc)}

  .fecha-portada{
    display:inline-block;margin-top:12px;padding:7px 24px;
    font-family:var(--titulo);font-weight:700;font-size:19px;line-height:1.25;color:var(--vino);
    background:#FFFDF9;border:3px solid var(--rosa);border-radius:999px;
    box-shadow:0 4px 0 rgba(196,102,127,.35);transform:rotate(-1deg);
  }
  .baja{
    position:absolute;left:0;right:0;bottom:12px;z-index:4;
    font-family:var(--mano);font-size:22px;color:var(--rosa-osc);
    animation:respirar 2.6s ease-in-out infinite;
  }
  @keyframes respirar{0%,100%{transform:translateY(0);opacity:.6}50%{transform:translateY(7px);opacity:1}}

  /* ---------- tarjetas con encaje ---------- */
  .tarjeta{
    position:relative;z-index:3;margin:0 auto;max-width:404px;
    background:var(--durazno);border:3px solid var(--rosa);border-radius:30px;
    box-shadow:0 7px 0 rgba(196,102,127,.28);
    padding:32px 26px 28px;text-align:center;
  }
  .tarjeta::after{
    content:"";position:absolute;top:8px;right:8px;bottom:8px;left:8px;
    border:2px dashed rgba(196,102,127,.45);border-radius:22px;pointer-events:none;
  }
  .tarjeta.clara{background:#FFFDF9}
  .tarjeta.torcida-1{transform:rotate(-1.2deg)}
  .tarjeta.torcida-2{transform:rotate(1.2deg)}
  .tarjeta > *{position:relative;z-index:1}

  .titulo{font-family:var(--titulo);font-weight:700;font-size:27px;line-height:1.2;color:var(--vino)}
  .subtitulo{font-family:var(--mano);font-size:27px;color:var(--salvia-osc);line-height:1.15}
  .texto{font-size:15.5px;max-width:32ch;margin:10px auto 0}
  .texto b{font-weight:700;color:var(--rosa-osc)}

  .sticker{position:absolute;width:80px;height:auto;z-index:4;pointer-events:none}
  .st-sup-izq{top:-38px;left:-6px}
  .st-sup-der{top:-40px;right:-4px}
  .st-inf-der{bottom:-30px;right:-8px}
  .st-inf-izq{bottom:-32px;left:-8px}

  /* cuenta regresiva */
  .cuenta{display:flex;justify-content:center;gap:9px;margin-top:14px}
  .cuenta div{
    flex:1;max-width:76px;background:#FFFDF9;border:3px solid var(--rosa);border-radius:20px;
    padding:9px 2px 7px;box-shadow:0 4px 0 rgba(196,102,127,.25);
  }
  .cuenta b{display:block;font-family:var(--titulo);font-weight:800;font-size:28px;line-height:1;color:var(--vino)}
  .cuenta span{font-family:var(--mano);font-size:17px;color:var(--rosa-osc)}

  /* fecha */
  .dia-grande{font-family:var(--script);font-size:66px;line-height:1;color:var(--vino)}
  .mes{font-family:var(--titulo);font-weight:700;font-size:23px;color:var(--rosa-osc);text-transform:uppercase;letter-spacing:.1em}
  .dia-semana{font-family:var(--mano);font-size:28px;color:var(--salvia-osc)}
  .hora{
    display:inline-block;margin-top:12px;padding:7px 22px;border-radius:999px;
    background:var(--salvia);color:#FFF8F2;font-family:var(--titulo);font-weight:700;font-size:17px;
    box-shadow:0 4px 0 rgba(97,117,76,.4);
  }

  /* botones */
  .btn{
    display:inline-block;margin-top:18px;padding:13px 26px;border:3px solid var(--rosa-osc);
    border-radius:999px;font-family:var(--titulo);font-weight:700;font-size:15px;
    color:var(--vino);text-decoration:none;background:#FFFDF9;
    box-shadow:0 5px 0 rgba(196,102,127,.35);
    transition:transform .12s ease,box-shadow .12s ease,background .2s ease,color .2s ease;
  }
  .btn:hover,.btn:focus-visible{background:var(--rosa-palo)}
  .btn:active{transform:translateY(4px);box-shadow:0 1px 0 rgba(196,102,127,.35)}
  .btn.salvia{background:var(--salvia);border-color:var(--salvia-osc);color:#FFF8F2}
  .btn.salvia:hover,.btn.salvia:focus-visible{background:var(--salvia-osc)}
  .btn.rosa{background:var(--rosa);border-color:var(--rosa-osc);color:#FFFDF9}
  .btn.rosa:hover,.btn.rosa:focus-visible{background:var(--rosa-osc)}
  a:focus-visible{outline:3px solid var(--dorado);outline-offset:3px}

  .camino{display:block;width:100%;max-width:404px;height:auto;margin:0 auto;position:relative;z-index:2}

  .cierre{text-align:center;position:relative;z-index:3;padding:26px 22px 0}
  .cierre .subtitulo{font-size:30px}
  .cierre .firma{font-family:var(--script);font-size:54px;color:var(--vino);line-height:1.2}

  .bosque-final{display:block;width:100%;height:auto;position:relative;z-index:2;margin-top:-6px}
  .pie{
    position:relative;z-index:3;padding:4px 24px 30px;text-align:center;
    font-family:var(--mano);font-size:20px;color:var(--rosa-osc);
  }

  .rev{opacity:0;transform:translateY(20px) scale(.97);transition:opacity .7s ease,transform .7s cubic-bezier(.34,1.56,.64,1)}
  .rev.dentro{opacity:1;transform:none}

  .flota{animation:flotar 4.4s ease-in-out infinite;transform-box:fill-box;transform-origin:center}
  .flota-2{animation:flotar 5.6s ease-in-out infinite;animation-delay:-1.8s;transform-box:fill-box;transform-origin:center}
  .flota-3{animation:flotar 6.4s ease-in-out infinite;animation-delay:-3.2s;transform-box:fill-box;transform-origin:center}
  @keyframes flotar{0%,100%{transform:translateY(0) rotate(-5deg)}50%{transform:translateY(-12px) rotate(5deg)}}
  .brinca{animation:brincar 2.8s ease-in-out infinite;transform-box:fill-box;transform-origin:bottom center}
  @keyframes brincar{0%,72%,100%{transform:translateY(0)}82%{transform:translateY(-9px)}92%{transform:translateY(0)}}
  .chispa{animation:brillar 2.4s ease-in-out infinite;transform-box:fill-box;transform-origin:center}
  .chispa:nth-of-type(2n){animation-delay:-1s}
  .chispa:nth-of-type(3n){animation-delay:-1.8s}
  @keyframes brillar{0%,100%{opacity:.25;transform:scale(.6)}50%{opacity:1;transform:scale(1.25)}}

  @media (prefers-reduced-motion:reduce){
    .rev{opacity:1;transform:none;transition:none}
    .hoja{display:none}
    .baja,.flota,.flota-2,.flota-3,.brinca,.chispa{animation:none!important}
  }
</style>
</head>
<body>

<!-- ================= DIBUJOS ================= -->
<svg class="sprites" aria-hidden="true" xmlns="http://www.w3.org/2000/svg">
<defs>
  <filter id="suave" x="-40%" y="-40%" width="180%" height="180%"><feGaussianBlur stdDeviation="5"/></filter>

  <!-- elementos de otoño -->
  <g id="baya">
    <path d="M-1,5 C-2,-3 -3,-9 -6,-14" stroke="#61754C" stroke-width="1.8" fill="none" stroke-linecap="round"/>
    <path d="M6,-13 C13,-15 16,-10 12,-6 C8,-4 5,-8 6,-13 Z" fill="#8A9E72" stroke="#6B4A3A" stroke-width="1.6" stroke-linejoin="round"/>
    <circle cx="-6" cy="-2" r="4.8" fill="#C4667F" stroke="#6B4A3A" stroke-width="1.8"/>
    <circle cx="3.4" cy="-5" r="4.4" fill="#E28BA2" stroke="#6B4A3A" stroke-width="1.8"/>
    <circle cx="-1" cy="5" r="4.2" fill="#B04A5A" stroke="#6B4A3A" stroke-width="1.8"/>
    <circle cx="-7.4" cy="-3.4" r="1.3" fill="#FFF8F2" opacity=".8"/>
    <circle cx="2.2" cy="-6.2" r="1.2" fill="#FFF8F2" opacity=".8"/>
  </g>
  <g id="ramita">
    <path d="M0,8 C1,-1 2,-10 1,-19" stroke="#A87A5E" stroke-width="2.2" fill="none" stroke-linecap="round"/>
    <g transform="translate(-7,-2) rotate(-42) scale(.62)">
      <path d="M0,-17 C8,-11 8,-2 0,3 C-8,-2 -8,-11 0,-17 Z" fill="#DC8A57" stroke="#6B4A3A" stroke-width="3.2" stroke-linejoin="round"/>
      <path d="M0,-15 V1.5" stroke="#6B4A3A" stroke-width="2.2"/>
    </g>
    <g transform="translate(8,-7) rotate(42) scale(.62)">
      <path d="M0,-17 C8,-11 8,-2 0,3 C-8,-2 -8,-11 0,-17 Z" fill="#E9A9B8" stroke="#6B4A3A" stroke-width="3.2" stroke-linejoin="round"/>
      <path d="M0,-15 V1.5" stroke="#6B4A3A" stroke-width="2.2"/>
    </g>
    <g transform="translate(0,-17) scale(.62)">
      <path d="M0,-17 C8,-11 8,-2 0,3 C-8,-2 -8,-11 0,-17 Z" fill="#EFC15E" stroke="#6B4A3A" stroke-width="3.2" stroke-linejoin="round"/>
      <path d="M0,-15 V1.5" stroke="#6B4A3A" stroke-width="2.2"/>
    </g>
  </g>

  <!-- moño -->
  <g id="mono">
    <path d="M-2.6,0 C-9,-9 -20,-8 -20,-1 C-20,6 -9,7 -2.6,0 Z" fill="#E28BA2" stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round"/>
    <path d="M2.6,0 C9,-9 20,-8 20,-1 C20,6 9,7 2.6,0 Z" fill="#E28BA2" stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round"/>
    <path d="M-3,2 C-6,10 -9,14 -12,17" stroke="#E28BA2" stroke-width="4" fill="none" stroke-linecap="round"/>
    <path d="M3,2 C6,10 9,14 12,17" stroke="#E28BA2" stroke-width="4" fill="none" stroke-linecap="round"/>
    <circle cx="0" cy="0" r="4.4" fill="#C4667F" stroke="#6B4A3A" stroke-width="2"/>
  </g>
  <g id="corazon">
    <path d="M0,7 C-9,0 -11,-6 -6.6,-9 C-3,-11.4 0,-8.4 0,-6 C0,-8.4 3,-11.4 6.6,-9 C11,-6 9,0 0,7 Z"
          fill="#E28BA2" stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round"/>
  </g>

  <!-- árbol alto de otoño -->
  <g id="arbolito">
    <path d="M-9,0 C-8,-16 -7,-32 -5,-48 C-4,-58 -3,-66 -3,-74 L3,-74 C3,-66 4,-58 5,-48 C7,-32 8,-16 9,0 Z"
          fill="#8A5E42" stroke="#5C3D2B" stroke-width="2.6" stroke-linejoin="round"/>
    <path d="M-5,-4 C-14,-2 -20,-1 -26,0 L26,0 C20,-1 14,-2 5,-4 Z" fill="#8A5E42" stroke="#5C3D2B" stroke-width="2.6" stroke-linejoin="round"/>
    <path d="M-2,-72 C-8,-92 -20,-108 -34,-120" stroke="#8A5E42" stroke-width="7.5" fill="none" stroke-linecap="round"/>
    <path d="M2,-74 C8,-94 20,-110 34,-122" stroke="#8A5E42" stroke-width="7.5" fill="none" stroke-linecap="round"/>
    <path d="M0,-74 C1,-100 1,-130 0,-158" stroke="#8A5E42" stroke-width="7" fill="none" stroke-linecap="round"/>
    <path d="M-22,-104 C-34,-108 -48,-104 -58,-96" stroke="#8A5E42" stroke-width="5" fill="none" stroke-linecap="round"/>
    <path d="M22,-106 C34,-110 48,-106 58,-98" stroke="#8A5E42" stroke-width="5" fill="none" stroke-linecap="round"/>
    <path d="M-30,-116 C-36,-128 -34,-142 -28,-152" stroke="#8A5E42" stroke-width="4.4" fill="none" stroke-linecap="round"/>
    <path d="M30,-118 C36,-130 34,-144 28,-154" stroke="#8A5E42" stroke-width="4.4" fill="none" stroke-linecap="round"/>
    <path d="M0,-130 C-8,-142 -18,-150 -26,-156" stroke="#8A5E42" stroke-width="3.8" fill="none" stroke-linecap="round"/>
    <path d="M0,-134 C8,-146 18,-154 26,-160" stroke="#8A5E42" stroke-width="3.8" fill="none" stroke-linecap="round"/>
    <path d="M0,-158 C-4,-168 -8,-174 -12,-178" stroke="#8A5E42" stroke-width="3.2" fill="none" stroke-linecap="round"/>
    <path d="M0,-158 C4,-168 8,-174 12,-178" stroke="#8A5E42" stroke-width="3.2" fill="none" stroke-linecap="round"/>
    <g stroke="#5C3D2B" stroke-width="1.6" stroke-linecap="round" opacity=".45">
      <path d="M-3,-20 C-2,-30 -3,-40 -2,-50"/><path d="M3,-26 C4,-36 3,-46 4,-56"/>
    </g>
    <g stroke="#B4823F" stroke-width=".7" stroke-opacity=".5">
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-21.4,-170.4) rotate(153) scale(0.90)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(8.0,-184.8) rotate(109) scale(0.90)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(13.7,-168.2) rotate(-147) scale(1.03)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-15.6,-185.1) rotate(-17) scale(1.00)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-19.6,-192.2) rotate(-157) scale(0.73)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-21.4,-189.2) rotate(-63) scale(0.94)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-23.8,-178.4) rotate(-0) scale(0.97)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-10.8,-189.4) rotate(18) scale(1.07)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-4.4,-189.8) rotate(-97) scale(0.83)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-9.1,-179.2) rotate(-141) scale(0.83)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(26.7,-182.1) rotate(-180) scale(0.80)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-29.2,-171.3) rotate(-37) scale(0.75)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(2.8,-189.0) rotate(-149) scale(0.85)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(0.5,-184.7) rotate(-91) scale(0.76)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-20.4,-172.1) rotate(66) scale(0.79)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(9.3,-155.7) rotate(-133) scale(0.96)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-23.6,-160.4) rotate(-180) scale(1.05)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-9.4,-153.4) rotate(-104) scale(0.87)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(24.1,-161.0) rotate(-103) scale(0.82)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(9.0,-189.9) rotate(-153) scale(0.80)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-11.9,-156.5) rotate(44) scale(0.77)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-52.6,-156.0) rotate(132) scale(0.79)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-35.3,-146.7) rotate(40) scale(1.00)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-31.9,-182.7) rotate(-109) scale(1.08)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-45.5,-168.0) rotate(-143) scale(0.73)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-28.2,-136.7) rotate(-87) scale(1.03)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-33.4,-147.7) rotate(79) scale(0.75)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-54.0,-155.3) rotate(42) scale(0.75)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-18.2,-163.7) rotate(-174) scale(0.82)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-30.0,-152.5) rotate(-78) scale(0.92)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-20.7,-152.8) rotate(-18) scale(0.85)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-39.7,-162.8) rotate(-167) scale(0.73)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-38.9,-181.8) rotate(-172) scale(0.96)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-14.7,-152.2) rotate(-131) scale(0.75)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-54.7,-164.3) rotate(144) scale(1.00)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-22.3,-181.5) rotate(-53) scale(0.98)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-16.6,-169.9) rotate(105) scale(1.05)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-5.7,-156.1) rotate(-43) scale(0.72)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-9.0,-148.2) rotate(178) scale(1.05)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(12.3,-145.9) rotate(29) scale(0.89)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(54.5,-148.9) rotate(-169) scale(0.95)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(61.1,-156.5) rotate(-139) scale(1.02)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(31.9,-157.3) rotate(-72) scale(0.98)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(6.1,-162.6) rotate(-57) scale(1.07)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(45.3,-169.2) rotate(60) scale(0.80)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(40.6,-180.9) rotate(-108) scale(0.80)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(17.4,-167.2) rotate(-131) scale(0.91)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(24.9,-184.1) rotate(-80) scale(0.78)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(3.6,-155.6) rotate(119) scale(0.87)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(15.2,-159.4) rotate(122) scale(1.09)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(20.3,-139.0) rotate(-80) scale(0.95)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(16.9,-166.1) rotate(105) scale(0.73)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(21.2,-153.8) rotate(97) scale(0.82)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(40.6,-184.2) rotate(-138) scale(0.76)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(16.9,-179.0) rotate(165) scale(0.98)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(38.8,-171.5) rotate(77) scale(1.01)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(29.2,-170.5) rotate(-82) scale(0.85)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(2.0,-160.1) rotate(-123) scale(1.04)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-28.1,-117.6) rotate(80) scale(0.77)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-43.1,-108.1) rotate(-178) scale(0.93)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-43.8,-152.9) rotate(-13) scale(0.97)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-30.1,-116.6) rotate(107) scale(1.07)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-45.7,-107.2) rotate(173) scale(1.09)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-24.3,-133.5) rotate(-86) scale(0.99)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-56.8,-124.2) rotate(-21) scale(0.93)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-56.9,-129.7) rotate(111) scale(0.74)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-44.2,-117.4) rotate(104) scale(0.77)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-24.5,-130.0) rotate(7) scale(0.98)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-32.8,-135.8) rotate(162) scale(0.75)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-72.1,-123.2) rotate(119) scale(0.93)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-78.4,-133.2) rotate(22) scale(0.84)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-26.0,-136.4) rotate(39) scale(0.84)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-31.4,-133.5) rotate(26) scale(0.80)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-50.5,-128.9) rotate(-44) scale(0.92)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-70.3,-131.6) rotate(108) scale(0.93)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-42.1,-124.4) rotate(155) scale(0.89)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(51.6,-115.2) rotate(-134) scale(0.88)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(44.6,-133.3) rotate(-29) scale(0.73)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(71.6,-116.2) rotate(-172) scale(0.79)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(69.4,-131.0) rotate(80) scale(0.81)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(73.6,-119.1) rotate(-136) scale(0.91)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(49.1,-152.2) rotate(136) scale(0.73)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(64.4,-149.2) rotate(14) scale(1.05)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(40.4,-145.7) rotate(126) scale(0.95)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(56.7,-110.9) rotate(112) scale(1.06)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(32.2,-146.0) rotate(-110) scale(1.02)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(62.1,-137.9) rotate(-94) scale(1.00)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(39.4,-121.5) rotate(159) scale(0.93)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(61.0,-113.4) rotate(108) scale(0.76)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(42.6,-153.4) rotate(169) scale(0.76)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(42.7,-142.8) rotate(179) scale(1.04)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(49.5,-131.6) rotate(94) scale(0.95)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(41.5,-130.7) rotate(-139) scale(0.79)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(81.9,-133.4) rotate(-146) scale(0.74)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-12.6,-134.7) rotate(-39) scale(0.88)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-38.9,-130.4) rotate(-175) scale(0.99)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-12.4,-124.0) rotate(86) scale(0.87)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-26.6,-142.3) rotate(105) scale(0.84)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-12.8,-156.3) rotate(130) scale(0.96)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-30.7,-142.3) rotate(30) scale(0.85)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-21.7,-130.3) rotate(87) scale(0.78)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-9.6,-128.2) rotate(14) scale(0.86)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-18.4,-152.6) rotate(80) scale(0.75)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-22.7,-131.1) rotate(140) scale(1.10)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-17.1,-115.8) rotate(60) scale(0.85)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-37.9,-145.1) rotate(-40) scale(1.10)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-27.1,-157.1) rotate(173) scale(0.73)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-21.0,-149.6) rotate(-35) scale(0.74)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-21.7,-139.9) rotate(-87) scale(0.82)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-38.3,-143.1) rotate(168) scale(0.94)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(8.3,-155.7) rotate(-153) scale(0.95)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(4.2,-125.4) rotate(-41) scale(1.09)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(3.9,-144.6) rotate(-25) scale(0.91)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(3.4,-143.0) rotate(-48) scale(0.83)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(10.7,-144.5) rotate(78) scale(0.83)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(26.9,-157.4) rotate(48) scale(0.88)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(38.3,-135.8) rotate(-37) scale(0.94)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(47.0,-130.3) rotate(-25) scale(0.90)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(32.1,-138.0) rotate(112) scale(1.07)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(48.2,-142.8) rotate(37) scale(0.76)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(12.3,-137.2) rotate(-161) scale(0.92)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(17.4,-133.5) rotate(-30) scale(0.95)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(17.3,-152.6) rotate(88) scale(1.03)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(46.1,-145.8) rotate(-94) scale(0.76)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(28.6,-157.7) rotate(-51) scale(0.82)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(20.3,-149.5) rotate(-80) scale(0.81)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-83.0,-100.2) rotate(-109) scale(0.98)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-48.8,-99.3) rotate(-170) scale(0.73)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-68.8,-101.5) rotate(-149) scale(0.98)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-59.5,-78.2) rotate(-6) scale(0.85)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-74.5,-84.1) rotate(122) scale(0.75)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-84.3,-93.5) rotate(122) scale(1.01)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-73.7,-94.9) rotate(112) scale(0.86)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-67.8,-81.4) rotate(117) scale(0.79)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-77.5,-107.3) rotate(-63) scale(0.93)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-78.7,-106.0) rotate(67) scale(0.83)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-51.3,-95.3) rotate(58) scale(0.75)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-84.7,-99.4) rotate(-62) scale(1.06)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-75.9,-85.3) rotate(-48) scale(0.76)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-84.6,-108.9) rotate(158) scale(1.07)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-87.4,-104.2) rotate(-15) scale(0.80)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(62.2,-88.7) rotate(-48) scale(0.86)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(42.0,-112.0) rotate(86) scale(0.86)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(39.0,-107.1) rotate(23) scale(0.79)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(72.1,-110.0) rotate(-172) scale(0.92)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(69.7,-91.9) rotate(-172) scale(1.04)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(79.7,-95.6) rotate(104) scale(0.75)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(60.8,-94.9) rotate(-67) scale(0.73)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(81.2,-90.5) rotate(-28) scale(0.99)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(63.8,-117.9) rotate(95) scale(0.87)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(67.3,-113.9) rotate(-131) scale(0.91)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(55.5,-122.4) rotate(-32) scale(1.03)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(76.1,-117.8) rotate(120) scale(1.06)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(50.0,-114.3) rotate(76) scale(1.02)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(84.1,-111.8) rotate(-92) scale(0.78)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(56.1,-113.5) rotate(-40) scale(0.92)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-27.8,-109.0) rotate(-69) scale(0.76)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-32.2,-117.2) rotate(-158) scale(0.89)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-57.1,-105.7) rotate(-67) scale(0.80)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-31.4,-97.5) rotate(78) scale(0.95)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-57.0,-100.5) rotate(-35) scale(1.07)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-51.6,-123.3) rotate(18) scale(1.04)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-15.1,-121.7) rotate(-57) scale(0.93)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-46.2,-106.9) rotate(-162) scale(1.08)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-11.1,-111.0) rotate(99) scale(1.02)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-41.0,-117.0) rotate(-176) scale(0.90)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-46.3,-104.6) rotate(-28) scale(1.05)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-25.9,-97.5) rotate(-87) scale(1.05)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-18.8,-94.0) rotate(43) scale(0.92)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-20.7,-92.3) rotate(-180) scale(1.03)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-30.7,-113.7) rotate(-83) scale(0.99)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(52.7,-121.8) rotate(-150) scale(1.00)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(44.9,-119.5) rotate(104) scale(0.88)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(39.4,-124.4) rotate(-167) scale(0.88)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(49.0,-93.1) rotate(-68) scale(0.84)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(11.6,-117.7) rotate(60) scale(0.75)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(32.7,-116.6) rotate(-38) scale(0.90)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(34.4,-112.0) rotate(-44) scale(0.99)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(33.6,-102.8) rotate(98) scale(1.05)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(44.3,-115.0) rotate(46) scale(1.08)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(57.7,-115.5) rotate(20) scale(0.75)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(42.9,-92.0) rotate(-61) scale(1.08)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(15.6,-106.7) rotate(-19) scale(0.87)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(41.1,-104.7) rotate(64) scale(0.99)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(37.7,-106.0) rotate(-13) scale(0.99)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(37.5,-101.3) rotate(-135) scale(0.87)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-12.8,-101.2) rotate(154) scale(0.77)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(2.5,-137.9) rotate(-41) scale(0.85)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-15.9,-131.2) rotate(41) scale(0.84)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-10.8,-132.6) rotate(-173) scale(0.85)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-6.0,-104.2) rotate(21) scale(0.80)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(5.7,-137.5) rotate(40) scale(0.78)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(15.8,-127.4) rotate(-53) scale(0.91)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-10.3,-122.4) rotate(156) scale(1.10)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-3.9,-119.5) rotate(57) scale(1.02)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(0.7,-101.2) rotate(71) scale(0.85)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-2.5,-97.3) rotate(-17) scale(1.00)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(15.8,-127.2) rotate(22) scale(0.93)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(11.0,-101.4) rotate(143) scale(0.85)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(16.9,-104.0) rotate(-76) scale(1.06)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-47.3,-89.3) rotate(-120) scale(0.95)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-61.4,-74.6) rotate(102) scale(1.07)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-54.4,-63.7) rotate(86) scale(0.87)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-60.2,-90.6) rotate(-123) scale(0.88)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-39.5,-68.9) rotate(25) scale(0.79)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-40.6,-71.2) rotate(155) scale(0.74)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-51.5,-94.3) rotate(-35) scale(0.91)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-61.9,-75.7) rotate(45) scale(0.98)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-47.8,-91.0) rotate(178) scale(1.04)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-44.6,-83.7) rotate(-139) scale(1.08)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-62.3,-79.9) rotate(146) scale(0.84)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(45.1,-65.9) rotate(-24) scale(0.86)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(50.1,-90.3) rotate(34) scale(0.75)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(56.1,-87.6) rotate(134) scale(1.09)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(44.6,-92.8) rotate(-94) scale(0.84)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(69.2,-86.4) rotate(180) scale(1.00)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(59.5,-89.0) rotate(110) scale(0.80)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(30.9,-87.2) rotate(-145) scale(1.02)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(62.3,-89.6) rotate(-17) scale(0.83)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(59.0,-78.8) rotate(-21) scale(0.89)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(39.5,-73.3) rotate(31) scale(0.74)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(38.2,-77.1) rotate(-63) scale(0.77)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-8.8,-97.8) rotate(129) scale(0.98)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-9.2,-75.9) rotate(-53) scale(0.90)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-28.1,-103.7) rotate(22) scale(0.92)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-8.6,-75.6) rotate(-162) scale(0.76)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-4.8,-94.4) rotate(-29) scale(1.05)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-23.1,-109.1) rotate(-20) scale(0.75)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-11.1,-97.0) rotate(69) scale(0.82)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-28.0,-92.1) rotate(-82) scale(1.03)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-3.4,-101.5) rotate(-98) scale(0.83)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-21.8,-100.5) rotate(50) scale(0.75)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(3.1,-89.0) rotate(11) scale(0.74)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(15.6,-84.9) rotate(109) scale(0.75)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(27.6,-94.6) rotate(-115) scale(1.00)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(26.1,-77.7) rotate(176) scale(0.73)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(32.6,-101.2) rotate(-179) scale(1.06)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(25.0,-81.4) rotate(52) scale(0.86)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(21.3,-107.2) rotate(2) scale(1.04)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(17.4,-107.6) rotate(34) scale(1.01)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(9.7,-99.7) rotate(-21) scale(1.01)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(17.0,-80.2) rotate(127) scale(0.95)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(19.6,-146.2) rotate(77) scale(0.94)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-9.2,-134.6) rotate(39) scale(1.03)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-12.4,-145.9) rotate(107) scale(0.75)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-17.4,-156.8) rotate(105) scale(0.81)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(16.0,-145.2) rotate(70) scale(1.03)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(4.4,-169.0) rotate(-1) scale(0.97)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(6.2,-140.2) rotate(-122) scale(0.98)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(15.4,-144.7) rotate(-49) scale(0.80)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(15.6,-136.1) rotate(36) scale(0.77)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-25.6,-153.0) rotate(-179) scale(0.88)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(10.3,-139.2) rotate(-73) scale(0.88)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(21.1,-153.2) rotate(78) scale(1.09)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-2.5,-142.7) rotate(128) scale(0.88)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(14.3,-155.5) rotate(-59) scale(1.09)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-29.2,-142.8) rotate(54) scale(0.74)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-64.9,-154.0) rotate(138) scale(1.07)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-58.6,-143.0) rotate(123) scale(0.86)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-40.9,-134.3) rotate(-114) scale(0.93)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-59.1,-144.4) rotate(34) scale(1.01)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-66.6,-139.4) rotate(65) scale(1.05)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-59.0,-149.3) rotate(-163) scale(0.83)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-56.5,-156.1) rotate(87) scale(0.91)" fill="#C4667F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-26.0,-154.0) rotate(-83) scale(0.86)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-46.9,-163.8) rotate(-131) scale(0.81)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-30.5,-144.5) rotate(-42) scale(0.75)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-53.6,-130.1) rotate(7) scale(0.74)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(32.9,-156.9) rotate(-112) scale(0.92)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(59.1,-145.7) rotate(-27) scale(0.93)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(28.3,-149.6) rotate(-67) scale(0.89)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(52.5,-140.6) rotate(-79) scale(0.99)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(57.3,-136.9) rotate(-52) scale(0.76)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(39.7,-140.2) rotate(-165) scale(0.73)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(26.2,-155.4) rotate(171) scale(0.83)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(55.7,-152.6) rotate(68) scale(0.97)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(47.8,-131.9) rotate(-148) scale(0.88)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(29.2,-147.4) rotate(155) scale(0.83)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(50.1,-128.7) rotate(-107) scale(1.01)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(40.0,-156.6) rotate(-147) scale(0.85)" fill="#F2D08A"/>
    </g>
    <g opacity=".9">
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(43.8,-35.2) rotate(-87) scale(0.86)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(28.8,-60.7) rotate(-39) scale(0.71)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(59.4,-46.8) rotate(-44) scale(0.85)" fill="#DC8A57"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-4.5,-43.8) rotate(-89) scale(0.61)" fill="#F2D08A"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-25.4,-41.1) rotate(-73) scale(0.84)" fill="#E8B14F"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(20.5,-40.5) rotate(-57) scale(0.87)" fill="#EFC15E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(11.0,-9.2) rotate(98) scale(0.79)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-12.8,-38.7) rotate(-81) scale(0.85)" fill="#D9945E"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-17.0,-11.1) rotate(-166) scale(0.64)" fill="#E9A9B8"/>
      <path d="M0,0 C-6.4,-2.6 -6.8,-9.6 0,-11.6 C6.8,-9.6 6.4,-2.6 0,0 Z" transform="translate(-32.7,-34.3) rotate(-10) scale(0.61)" fill="#E8B14F"/>
    </g>
    <g stroke="#61754C" stroke-width="2" stroke-linecap="round" fill="none">
      <path d="M-24,0 C-26,-6 -25,-9 -23,-12"/><path d="M-18,0 C-19,-7 -18,-11 -16,-14"/>
      <path d="M18,0 C19,-7 18,-11 16,-14"/><path d="M24,0 C26,-6 25,-9 23,-12"/>
    </g>
  </g>

  <g id="mata">
    <path d="M-30,0 C-32,-20 -18,-30 -6,-26 C0,-38 18,-38 22,-24 C34,-24 36,-8 30,0 Z"
          fill="#8A9E72" stroke="#61754C" stroke-width="3" stroke-linejoin="round"/>
    <use href="#baya" transform="translate(-13,-16) scale(.85)"/>
    <use href="#hojita" transform="translate(9,-20) rotate(14) scale(.7)"/>
    <use href="#hojita-rosa" transform="translate(22,-10) rotate(-16) scale(.65)"/>
  </g>

  <g id="helecho">
    <path d="M0,0 C7,-18 9,-38 5,-58" stroke="#61754C" stroke-width="2.4" fill="none" stroke-linecap="round"/>
    <ellipse cx="4" cy="-9" rx="9" ry="3.4" fill="#8A9E72" stroke="#61754C" stroke-width="1.6" transform="rotate(18 4 -9)"/>
    <ellipse cx="6" cy="-21" rx="8" ry="3" fill="#8A9E72" stroke="#61754C" stroke-width="1.6" transform="rotate(12 6 -21)"/>
    <ellipse cx="6" cy="-33" rx="6.6" ry="2.6" fill="#8A9E72" stroke="#61754C" stroke-width="1.5" transform="rotate(6 6 -33)"/>
    <ellipse cx="1" cy="-14" rx="8" ry="3" fill="#8A9E72" stroke="#61754C" stroke-width="1.6" transform="rotate(-24 1 -14)"/>
    <ellipse cx="1" cy="-27" rx="6.6" ry="2.6" fill="#8A9E72" stroke="#61754C" stroke-width="1.5" transform="rotate(-18 1 -27)"/>
    <ellipse cx="3" cy="-40" rx="5" ry="2.2" fill="#8A9E72" stroke="#61754C" stroke-width="1.4" transform="rotate(-10 3 -40)"/>
  </g>

  <!-- hongo con carita y moñito -->
  <g id="hongo">
    <path d="M-5,0 L-4.4,-13 C-4.4,-16 4.4,-16 4.4,-13 L5,0 Z" fill="#FFFDF9" stroke="#6B4A3A" stroke-width="2.4" stroke-linejoin="round"/>
    <path d="M-16,-13 C-16,-30 16,-30 16,-13 Z" fill="#E28BA2" stroke="#6B4A3A" stroke-width="2.6" stroke-linejoin="round"/>
    <circle cx="-7" cy="-20" r="3" fill="#FFF8F2"/>
    <circle cx="2.5" cy="-23" r="2.4" fill="#FFF8F2"/>
    <circle cx="9" cy="-17.5" r="2" fill="#FFF8F2"/>
    <circle cx="-3.4" cy="-8" r="1.2" fill="#6B4A3A"/>
    <circle cx="3.4" cy="-8" r="1.2" fill="#6B4A3A"/>
    <path d="M-2,-5 C0,-3.4 2,-3.4 3,-5" stroke="#6B4A3A" stroke-width="1.2" fill="none" stroke-linecap="round"/>
    <use href="#mono" transform="translate(-13,-26) scale(.42)"/>
  </g>

  <!-- venadita con corona de flores -->
  <g id="venado">
    <g stroke="#6B4A3A" stroke-width="2.6" stroke-linejoin="round">
      <rect x="-18" y="-27" width="8" height="29" rx="4" fill="#C99878"/>
      <rect x="-5" y="-27" width="8" height="29" rx="4" fill="#C99878"/>
      <rect x="8" y="-27" width="8" height="29" rx="4" fill="#D9AB8B"/>
      <rect x="19" y="-27" width="8" height="29" rx="4" fill="#D9AB8B"/>
      <ellipse cx="-24" cy="-42" rx="6.4" ry="7.4" fill="#FFF3EA"/>
      <ellipse cx="0" cy="-42" rx="26" ry="18" fill="#D9AB8B"/>
      <path d="M13,-50 C18,-58 22,-64 25,-69 L37,-62 C33,-57 28,-50 25,-46 Z" fill="#D9AB8B"/>
      <ellipse cx="34" cy="-73" rx="12.5" ry="10.5" fill="#D9AB8B"/>
      <ellipse cx="24" cy="-83" rx="8.4" ry="5" fill="#C08B6A" transform="rotate(-30 24 -83)"/>
      <ellipse cx="40" cy="-85" rx="7.6" ry="4.4" fill="#C08B6A" transform="rotate(26 40 -85)"/>
    </g>
    <ellipse cx="43" cy="-68" rx="7" ry="5.6" fill="#EFCDB4"/>
    <ellipse cx="45.5" cy="-68" rx="2.6" ry="2" fill="#6B4A3A"/>
    <circle cx="35" cy="-76" r="2.6" fill="#3B2A1E"/>
    <circle cx="36" cy="-77" r="1" fill="#FFF"/>
    <circle cx="28" cy="-69" r="3.4" fill="#E28BA2" opacity=".55"/>
    <g fill="#FFF3EA"><circle cx="-8" cy="-49" r="3"/><circle cx="1" cy="-52" r="2.6"/><circle cx="10" cy="-49" r="2.8"/><circle cx="-15" cy="-43" r="2.4"/></g>
    <use href="#ramita" transform="translate(27,-88) scale(.55)"/>
    <use href="#baya" transform="translate(36,-91) scale(.5)"/>
    <use href="#hojita-rosa" transform="translate(45,-88) scale(.6)"/>
    <use href="#mono" transform="translate(-22,-50) scale(.4)"/>
  </g>

  <!-- conejita con moño -->
  <g id="conejo">
    <g stroke="#6B4A3A" stroke-width="2.6" stroke-linejoin="round">
      <circle cx="-15" cy="-9" r="6.4" fill="#FFF3EA"/>
      <ellipse cx="0" cy="-17" rx="15" ry="17" fill="#F6E6DC"/>
      <ellipse cx="-4" cy="-52" rx="4.6" ry="13" fill="#F6E6DC" transform="rotate(-11 -4 -52)"/>
      <ellipse cx="9" cy="-53" rx="4.4" ry="13" fill="#F6E6DC" transform="rotate(10 9 -53)"/>
      <circle cx="2" cy="-37" r="12" fill="#F6E6DC"/>
      <ellipse cx="-2" cy="-2.5" rx="7" ry="3.8" fill="#FFF3EA"/>
      <ellipse cx="9" cy="-3" rx="6" ry="3.4" fill="#FFF3EA"/>
    </g>
    <ellipse cx="-4" cy="-52" rx="1.9" ry="8" fill="#E9A9B8" transform="rotate(-11 -4 -52)"/>
    <ellipse cx="9" cy="-53" rx="1.8" ry="8" fill="#E9A9B8" transform="rotate(10 9 -53)"/>
    <circle cx="-2.4" cy="-38.5" r="2.4" fill="#3B2A1E"/>
    <circle cx="-1.5" cy="-39.6" r=".9" fill="#FFF"/>
    <circle cx="7.6" cy="-38.5" r="2.4" fill="#3B2A1E"/>
    <circle cx="8.5" cy="-39.6" r=".9" fill="#FFF"/>
    <ellipse cx="2.6" cy="-33" rx="2.4" ry="1.8" fill="#D9758C"/>
    <circle cx="-8" cy="-33" r="3.4" fill="#E28BA2" opacity=".5"/>
    <circle cx="13" cy="-33" r="3.4" fill="#E28BA2" opacity=".5"/>
    <use href="#mono" transform="translate(13,-58) rotate(14) scale(.5)"/>
  </g>

  <!-- ardilla con florecita -->
  <g id="ardilla">
    <path d="M-8,-6 C-31,-9 -34,-46 -11,-51 C-22,-41 -24,-18 -6,-15 Z" fill="#C98A63" stroke="#6B4A3A" stroke-width="2.6" stroke-linejoin="round"/>
    <g stroke="#6B4A3A" stroke-width="2.6" stroke-linejoin="round">
      <ellipse cx="2" cy="-18" rx="13" ry="16" fill="#D89C72"/>
      <circle cx="6" cy="-37" r="10.4" fill="#D89C72"/>
      <ellipse cx="0.5" cy="-46" rx="3.6" ry="5.2" fill="#C98A63" transform="rotate(-16 0.5 -46)"/>
      <ellipse cx="11" cy="-46.5" rx="3.4" ry="5" fill="#C98A63" transform="rotate(14 11 -46.5)"/>
    </g>
    <ellipse cx="4" cy="-15" rx="8" ry="9.4" fill="#F6E2CE"/>
    <circle cx="9" cy="-38.5" r="2.4" fill="#3B2A1E"/>
    <circle cx="9.9" cy="-39.6" r=".9" fill="#FFF"/>
    <circle cx="2.6" cy="-38.5" r="2.2" fill="#3B2A1E"/>
    <ellipse cx="14" cy="-35" rx="2.2" ry="1.7" fill="#6B4A3A"/>
    <circle cx="0" cy="-32" r="3" fill="#E28BA2" opacity=".5"/>
    <g stroke="#6B4A3A" stroke-width="2.2" stroke-linejoin="round">
      <ellipse cx="15" cy="-22" rx="5.2" ry="6" fill="#DCA95A"/>
      <path d="M9.6,-25.6 C9.6,-30 20.4,-30 20.4,-25.6 Z" fill="#A87A5E"/>
    </g>
    <use href="#hojita-rosa" transform="translate(-1,-48) scale(.8)"/>
  </g>

  <g id="mariposa">
    <g stroke="#6B4A3A" stroke-width="1.8" stroke-linejoin="round">
      <ellipse cx="-6.5" cy="-5" rx="7" ry="5.6" fill="#E9A9B8" transform="rotate(-22 -6.5 -5)"/>
      <ellipse cx="6.5" cy="-5" rx="7" ry="5.6" fill="#E9A9B8" transform="rotate(22 6.5 -5)"/>
      <ellipse cx="-5" cy="3.6" rx="5" ry="4.2" fill="#EFC15E"/>
      <ellipse cx="5" cy="3.6" rx="5" ry="4.2" fill="#EFC15E"/>
      <ellipse cx="0" cy="-0.5" rx="1.8" ry="7.4" fill="#6B4A3A"/>
    </g>
    <path d="M-0.8,-7.4 C-2.8,-10.4 -5,-11.4 -6.6,-11.8 M0.8,-7.4 C2.8,-10.4 5,-11.4 6.6,-11.8"
          stroke="#6B4A3A" stroke-width="1.4" fill="none" stroke-linecap="round"/>
    <circle cx="-6.6" cy="-12.6" r="1.4" fill="#6B4A3A"/>
    <circle cx="6.6" cy="-12.6" r="1.4" fill="#6B4A3A"/>
  </g>

  <g id="pajaro">
    <g stroke="#6B4A3A" stroke-width="2.2" stroke-linejoin="round">
      <ellipse cx="0" cy="-8" rx="11" ry="9" fill="#E9A9B8"/>
      <circle cx="8" cy="-15" r="6.4" fill="#E9A9B8"/>
      <path d="M-9,-10 C-16,-16 -20,-14 -22,-10 C-18,-6 -13,-5 -9,-7 Z" fill="#D9758C"/>
    </g>
    <path d="M14,-15 l6,2 -6,2 Z" fill="#EFC15E" stroke="#6B4A3A" stroke-width="1.6" stroke-linejoin="round"/>
    <circle cx="10" cy="-17" r="1.8" fill="#3B2A1E"/>
    <path d="M-3,0 v4 M3,0 v4" stroke="#EFC15E" stroke-width="2.2" stroke-linecap="round"/>
    <use href="#hojita-rosa" transform="translate(4,-23) scale(.6)"/>
  </g>

  <!-- hada con corona de flores y vestido rosa -->
  <g id="hada">
    <g stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round">
      <ellipse cx="-12" cy="-36" rx="10" ry="15" fill="#FFF9F4" opacity=".95" transform="rotate(-24 -12 -36)"/>
      <ellipse cx="12" cy="-36" rx="10" ry="15" fill="#FFF9F4" opacity=".95" transform="rotate(24 12 -36)"/>
      <ellipse cx="-9" cy="-20" rx="7" ry="10" fill="#FFF9F4" opacity=".95" transform="rotate(-16 -9 -20)"/>
      <ellipse cx="9" cy="-20" rx="7" ry="10" fill="#FFF9F4" opacity=".95" transform="rotate(16 9 -20)"/>
      <path d="M0,-36 C8,-25 13,-11 14,-3 L-14,-3 C-13,-11 -8,-25 0,-36 Z" fill="#E9A9B8"/>
      <path d="M-14,-3 C-9,-7 -4,-4 0,-7 C4,-4 9,-7 14,-3 Z" fill="#E28BA2"/>
      <circle cx="0" cy="-45" r="9" fill="#F7DCC4"/>
    </g>
    <path d="M-7,-30 C-13,-26 -15,-21 -16,-17" stroke="#F7DCC4" stroke-width="3.6" fill="none" stroke-linecap="round"/>
    <path d="M7,-30 C13,-27 16,-24 18,-21" stroke="#F7DCC4" stroke-width="3.6" fill="none" stroke-linecap="round"/>
    <path d="M-4.6,-3 L-4.6,3 M4.6,-3 L4.6,3" stroke="#F7DCC4" stroke-width="3.6" stroke-linecap="round"/>
    <path d="M-9,-45 C-9,-58 9,-58 9,-45 C7,-50 -7,-50 -9,-45 Z" fill="#A87A5E" stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round"/>
    <circle cx="-9.4" cy="-49" r="4.6" fill="#A87A5E" stroke="#6B4A3A" stroke-width="2"/>
    <circle cx="9.4" cy="-49" r="4.6" fill="#A87A5E" stroke="#6B4A3A" stroke-width="2"/>
    <circle cx="-3" cy="-44.5" r="1.8" fill="#3B2A1E"/>
    <circle cx="3" cy="-44.5" r="1.8" fill="#3B2A1E"/>
    <path d="M-2.6,-40 C-1,-38.4 1,-38.4 2.6,-40" stroke="#3B2A1E" stroke-width="1.3" fill="none" stroke-linecap="round"/>
    <circle cx="-6.4" cy="-41.4" r="2.2" fill="#E28BA2" opacity=".6"/>
    <circle cx="6.4" cy="-41.4" r="2.2" fill="#E28BA2" opacity=".6"/>
    <use href="#ramita" transform="translate(-8,-55) scale(.5)"/>
    <use href="#baya" transform="translate(1,-58) scale(.45)"/>
    <use href="#hojita-rosa" transform="translate(9,-55) scale(.6)"/>
    <path d="M18,-21 L26,-31" stroke="#A87A5E" stroke-width="2.2" stroke-linecap="round"/>
    <use href="#corazon" transform="translate(28,-34) scale(.85)"/>
  </g>

  <g id="hojita">
    <path d="M0,-17 C8,-11 8,-2 0,3 C-8,-2 -8,-11 0,-17 Z" fill="#DC8A57" stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round"/>
    <path d="M0,-15 V1.5" stroke="#6B4A3A" stroke-width="1.4"/>
  </g>
  <g id="hojita-verde">
    <path d="M0,-17 C8,-11 8,-2 0,3 C-8,-2 -8,-11 0,-17 Z" fill="#8A9E72" stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round"/>
    <path d="M0,-15 V1.5" stroke="#6B4A3A" stroke-width="1.4"/>
  </g>
  <g id="hojita-rosa">
    <path d="M0,-17 C8,-11 8,-2 0,3 C-8,-2 -8,-11 0,-17 Z" fill="#E9A9B8" stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round"/>
    <path d="M0,-15 V1.5" stroke="#6B4A3A" stroke-width="1.4"/>
  </g>
  <g id="bellota">
    <ellipse cx="0" cy="-5" rx="6" ry="7" fill="#DCA95A" stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round"/>
    <path d="M-7.6,-10 C-7.6,-16 7.6,-16 7.6,-10 Z" fill="#A87A5E" stroke="#6B4A3A" stroke-width="2" stroke-linejoin="round"/>
    <path d="M0,-16 V-19.6" stroke="#6B4A3A" stroke-width="2" stroke-linecap="round"/>
  </g>
  <g id="huella">
    <ellipse cx="0" cy="0" rx="4.4" ry="3.4" fill="#E28BA2" opacity=".5"/>
    <circle cx="-4" cy="-5" r="1.6" fill="#E28BA2" opacity=".5"/>
    <circle cx="0" cy="-6.4" r="1.6" fill="#E28BA2" opacity=".5"/>
    <circle cx="4" cy="-5" r="1.6" fill="#E28BA2" opacity=".5"/>
  </g>
</defs>
</svg>

<div class="lienzo">

  <!-- ================= GUIRNALDA DE FLORES ================= -->
  <svg class="guirnalda" viewBox="0 0 400 104" aria-hidden="true">
    <path d="M0,10 C70,54 150,56 200,44 C250,32 330,48 400,14" stroke="#61754C" stroke-width="2.6" fill="none"/>
    <path d="M0,18 C70,62 150,64 200,52 C250,40 330,56 400,22" stroke="#8A9E72" stroke-width="2" fill="none" opacity=".7"/>
    <use href="#hojita-verde" transform="translate(28,30) rotate(-20) scale(.8)"/>
    <use href="#ramita" transform="translate(56,40) scale(.95)"/>
    <use href="#hojita-verde" transform="translate(84,50) rotate(18) scale(.75)"/>
    <use href="#baya" transform="translate(112,54) scale(1)"/>
    <use href="#hojita-rosa" transform="translate(140,58) rotate(-14) scale(.8)"/>
    <use href="#hojita-rosa" transform="translate(168,60) scale(1.1)"/>
    <use href="#mono" transform="translate(200,50) scale(.75)"/>
    <use href="#hojita-rosa" transform="translate(232,56) scale(1)"/>
    <use href="#hojita-verde" transform="translate(258,52) rotate(16) scale(.75)"/>
    <use href="#ramita" transform="translate(286,50) scale(.9)"/>
    <use href="#hojita" transform="translate(314,44) rotate(-16) scale(.8)"/>
    <use href="#baya" transform="translate(342,38) scale(.9)"/>
    <use href="#hojita-verde" transform="translate(370,26) rotate(20) scale(.75)"/>
  </svg>

  <!-- ================= PORTADA ================= -->
  <header class="portada">
    <svg class="cielo" viewBox="0 0 400 560" preserveAspectRatio="xMidYMax meet" aria-hidden="true">
      <circle cx="200" cy="120" r="152" fill="#FDEBE1" opacity=".75"/>
      <use href="#arbolito" transform="translate(28,560) scale(1)"/>
      <use href="#arbolito" transform="translate(374,562) scale(1.05)"/>
      <use href="#arbolito" transform="translate(150,540) scale(.5)" opacity=".85"/>
      <use href="#arbolito" transform="translate(256,538) scale(.44)" opacity=".85"/>
      <path d="M-10,560 C90,520 300,520 410,558 L410,600 L-10,600 Z" fill="#A3B586" stroke="#61754C" stroke-width="3"/>
      <path d="M-10,572 C90,536 300,536 410,570" stroke="#FFF8F2" stroke-width="3" fill="none" opacity=".5"/>
      <use href="#mata" transform="translate(46,556) scale(.95)"/>
      <use href="#mata" transform="translate(356,558) scale(1)"/>
      <use href="#helecho" transform="translate(104,556) scale(1.1)"/>
      <use href="#helecho" transform="translate(292,554) scale(1.05)"/>
      <use href="#ramita" transform="translate(80,552) scale(.9)"/>
      <use href="#baya" transform="translate(248,552) scale(.85)"/>
      <use href="#hojita-rosa" transform="translate(330,552) scale(1)"/>
      <use href="#venado" transform="translate(268,552) scale(1.15)"/>
      <g transform="translate(126,554) scale(1.05)"><use href="#conejo" class="brinca"/></g>
      <use href="#ardilla" transform="translate(186,552) scale(1)"/>
      <use href="#hongo" transform="translate(222,554) scale(1.05)"/>
      <use href="#hongo" transform="translate(240,558) scale(.7)"/>
      <use href="#bellota" transform="translate(160,556) scale(.95)"/>
      <g transform="translate(88,470) scale(1)"><use href="#pajaro" class="flota-3"/></g>
      <g transform="translate(318,436) scale(1.15)"><use href="#hada" class="flota"/></g>
      <g transform="translate(102,392) scale(1.2)"><use href="#mariposa" class="flota-2"/></g>
      <g transform="translate(266,346) scale(1)"><use href="#mariposa" class="flota-3"/></g>
      <g transform="translate(148,318) scale(.85)"><use href="#corazon" class="flota-2"/></g>
      <g transform="translate(302,290) scale(.7)"><use href="#corazon" class="flota-3"/></g>
      <g fill="#EFC15E">
        <circle class="chispa" cx="298" cy="392" r="3"/>
        <circle class="chispa" cx="342" cy="360" r="2.4"/>
        <circle class="chispa" cx="272" cy="440" r="2.6"/>
        <circle class="chispa" cx="128" cy="344" r="2.4"/>
        <circle class="chispa" cx="196" cy="300" r="2.2"/>
      </g>
    </svg>

    <div class="contenido">
      <p class="saludo">¡Ven al bosque a jugar!</p>
      <div class="nombre-wrap">
        <h1 class="nombre">Lilian</h1>
        <svg class="subrayado" viewBox="0 0 240 26" aria-hidden="true">
          <path d="M14,14 C70,4 170,4 226,14" stroke="#E28BA2" stroke-width="2.4" fill="none" stroke-linecap="round"/>
          <use href="#hojita-verde" transform="translate(30,16) rotate(-30) scale(.6)"/>
          <use href="#baya" transform="translate(50,12) scale(.62)"/>
          <use href="#hojita-rosa" transform="translate(120,8) scale(.8)"/>
          <use href="#ramita" transform="translate(190,12) scale(.62)"/>
          <use href="#hojita-verde" transform="translate(210,16) rotate(30) scale(.6)"/>
        </svg>
      </div>
      <div class="insignia">
        <svg class="corona" viewBox="0 0 110 110" aria-hidden="true">
          <circle cx="55" cy="55" r="41" fill="#FFFDF9" opacity=".9" stroke="#E28BA2" stroke-width="2.5"/>
          <use href="#ramita" transform="translate(55,10) scale(.72)"/>
          <use href="#baya" transform="translate(30,19) scale(.66)"/>
          <use href="#baya" transform="translate(80,19) scale(.66)"/>
          <use href="#hojita-rosa" transform="translate(13,44) scale(.85)"/>
          <use href="#hojita-rosa" transform="translate(97,44) scale(.85)"/>
          <use href="#hojita-verde" transform="translate(16,74) rotate(-40) scale(.6)"/>
          <use href="#hojita-verde" transform="translate(94,74) rotate(40) scale(.6)"/>
          <use href="#mono" transform="translate(55,100) scale(.62)"/>
        </svg>
        <b>2</b><span>añitos</span>
      </div>
      <p class="fecha-portada">Sábado 3 de octubre</p>
    </div>
    <p class="baja">↓ desliza ↓</p>
  </header>

  <!-- ================= INVITACIÓN ================= -->
  <div style="height:16px"></div>
  <section class="tarjeta torcida-1 rev">
    <svg class="sticker st-sup-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#ramita" transform="translate(30,50) scale(1.3)"/>
      <use href="#baya" transform="translate(52,58) scale(1.1)"/>
      <use href="#hojita-verde" transform="translate(44,40) rotate(24) scale(.9)"/>
    </svg>
    <svg class="sticker st-sup-der" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#mono" transform="translate(40,50) scale(1.1)"/>
    </svg>
    <p class="subtitulo">Las hojas ya se pintaron de oro</p>
    <p class="texto">y eso solo puede significar una cosa: <b>¡cumplo dos años!</b> Te invito a mi fiesta entre hadas, hojas doradas y animalitos.</p>
    <svg viewBox="0 0 300 96" style="width:100%;height:auto;margin-top:6px" aria-hidden="true">
      <path d="M20,88 C90,78 210,78 280,88" stroke="#61754C" stroke-width="2.2" fill="none" opacity=".45"/>
      <g transform="translate(96,88) scale(.95)"><use href="#conejo" class="brinca"/></g>
      <use href="#helecho" transform="translate(128,88) scale(.75)"/>
      <use href="#hongo" transform="translate(150,88) scale(.85)"/>
      <use href="#ramita" transform="translate(172,82) scale(.8)"/>
      <use href="#ardilla" transform="translate(200,88) scale(.9)"/>
      <g transform="translate(64,44) scale(.85)"><use href="#corazon" class="flota"/></g>
    </svg>
  </section>

  <svg class="camino" viewBox="0 0 300 44" aria-hidden="true">
    <use href="#huella" transform="translate(90,30) rotate(12)"/>
    <use href="#huella" transform="translate(118,18) rotate(12)"/>
    <use href="#hojita-rosa" transform="translate(150,24) scale(.9)"/>
    <use href="#huella" transform="translate(182,18) rotate(-8)"/>
    <use href="#huella" transform="translate(212,30) rotate(6)"/>
  </svg>

  <!-- ================= CUENTA REGRESIVA ================= -->
  <section class="tarjeta clara torcida-2 rev">
    <svg class="sticker st-sup-der" viewBox="0 0 80 80" aria-hidden="true">
      <g transform="translate(38,52) scale(1.5)"><use href="#pajaro" class="flota-2"/></g>
    </svg>
    <p class="titulo">Ya casi es el día</p>
    <div class="cuenta" id="cuenta">
      <div><b data-c="d">00</b><span>días</span></div>
      <div><b data-c="h">00</b><span>horas</span></div>
      <div><b data-c="m">00</b><span>min</span></div>
      <div><b data-c="s">00</b><span>seg</span></div>
    </div>
    <svg class="sticker st-inf-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#hongo" transform="translate(28,66) scale(1.3)"/>
      <use href="#hojita-rosa" transform="translate(52,62) scale(1.1)"/>
    </svg>
  </section>

  <div style="height:26px"></div>

  <!-- ================= LA CITA ================= -->
  <section class="tarjeta torcida-1 rev">
    <svg class="sticker st-sup-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#baya" transform="translate(32,52) scale(1.2)"/>
      <use href="#hojita-verde" transform="translate(50,48) rotate(28) scale(.95)"/>
    </svg>
    <p class="dia-semana">Sábado</p>
    <p class="dia-grande">3</p>
    <p class="mes">Octubre 2026</p>
    <p><span class="hora">3:00 de la tarde</span></p>
    <a class="btn" id="btn-calendario" href="#" target="_blank" rel="noopener">Agendar el día</a>
    <svg class="sticker st-inf-der" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#ardilla" transform="translate(34,72) scale(1.1)"/>
    </svg>
  </section>

  <svg class="camino" viewBox="0 0 300 44" aria-hidden="true">
    <use href="#huella" transform="translate(88,20) rotate(-10)"/>
    <use href="#huella" transform="translate(120,32) rotate(-10)"/>
    <use href="#corazon" transform="translate(152,22) scale(.7)"/>
    <use href="#huella" transform="translate(184,32) rotate(8)"/>
    <use href="#huella" transform="translate(214,20) rotate(-6)"/>
  </svg>

  <!-- ================= EL LUGAR ================= -->
  <section class="tarjeta clara torcida-2 rev">
    <svg class="sticker st-sup-der" viewBox="0 0 80 80" aria-hidden="true">
      <g transform="translate(40,52) scale(1.6)"><use href="#mariposa" class="flota-3"/></g>
    </svg>
    <p class="titulo">Nos vemos aquí</p>
    <p class="subtitulo" style="margin-top:6px">Terraza del Coto 11<br>Paseo de los Parques</p>
    <p class="texto">Av. San Blas 2285, Santa Cruz del Valle, Tlaquepaque, Jalisco</p>
    <a class="btn salvia" href="https://maps.app.goo.gl/nrrdH24tucgffceq8" target="_blank" rel="noopener">Cómo llegar</a>
    <svg class="sticker st-inf-izq" viewBox="0 0 80 80" aria-hidden="true">
      <g transform="translate(38,74) scale(1)"><use href="#conejo" class="brinca"/></g>
    </svg>
  </section>

  <div style="height:30px"></div>

  <!-- ================= REGALOS ================= -->
  <section class="tarjeta torcida-1 rev">
    <svg class="sticker st-sup-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#mono" transform="translate(38,50) scale(1.05)"/>
      <use href="#hojita-rosa" transform="translate(16,58) scale(1)"/>
    </svg>
    <p class="titulo">Regalos</p>
    <p class="texto">Tu presencia es nuestro mejor regalo. Esta lista es solo una guía de opciones si deseas tener un detalle con Lilian. ¡Gracias por tu cariño! ✨🤍</p>
    <a class="btn" href="https://www.amazon.com.mx/hz/wishlist/ls/1FPXL1FS1TXNE?ref_=wl_share" target="_blank" rel="noopener">Ver lista en Amazon</a>
    <svg class="sticker st-inf-der" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#venado" transform="translate(22,74) scale(.8)"/>
    </svg>
  </section>

  <svg class="camino" viewBox="0 0 300 44" aria-hidden="true">
    <use href="#huella" transform="translate(92,30) rotate(10)"/>
    <use href="#hojita-rosa" transform="translate(124,20) scale(.9)"/>
    <use href="#huella" transform="translate(156,30) rotate(-8)"/>
    <use href="#huella" transform="translate(188,18) rotate(-8)"/>
  </svg>

  <!-- ================= CONFIRMACIÓN ================= -->
  <section class="tarjeta clara torcida-2 rev">
    <svg class="sticker st-sup-der" viewBox="0 0 80 80" aria-hidden="true">
      <g transform="translate(38,68) scale(.95)"><use href="#hada" class="flota"/></g>
    </svg>
    <p class="titulo">¿Nos acompañas?</p>
    <p class="texto">Avísanos cuántos vienen antes del <b id="limite">26 de septiembre</b> para apartar su lugar en el bosque.</p>
    <a class="btn rosa" id="btn-whatsapp" href="#" target="_blank" rel="noopener">Confirmar por WhatsApp</a>
    <svg class="sticker st-inf-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#hongo" transform="translate(30,68) scale(1.2)"/>
      <use href="#ramita" transform="translate(54,62) scale(.95)"/>
    </svg>
  </section>

  <!-- ================= CIERRE ================= -->
  <div class="cierre rev">
    <p class="subtitulo">¡Te espero en el bosque!</p>
    <p class="firma">Lilian</p>
  </div>

  <svg class="bosque-final" viewBox="0 0 400 180" aria-hidden="true">
    <use href="#arbolito" transform="translate(28,170) scale(.72)"/>
    <use href="#arbolito" transform="translate(372,170) scale(.76)"/>
    <use href="#arbolito" transform="translate(178,156) scale(.42)" opacity=".85"/>
    <use href="#arbolito" transform="translate(264,154) scale(.38)" opacity=".85"/>
    <path d="M-10,168 C90,138 300,138 410,166 L410,200 L-10,200 Z" fill="#A3B586" stroke="#61754C" stroke-width="3"/>
    <path d="M-10,178 C90,150 300,150 410,176" stroke="#FFF8F2" stroke-width="3" fill="none" opacity=".5"/>
    <use href="#mata" transform="translate(200,166) scale(.85)"/>
    <use href="#helecho" transform="translate(64,164) scale(.95)"/>
    <g transform="translate(96,164) scale(.85)"><use href="#conejo" class="brinca"/></g>
    <use href="#hongo" transform="translate(136,164) scale(.9)"/>
    <use href="#ramita" transform="translate(158,158) scale(.85)"/>
    <use href="#ardilla" transform="translate(240,164) scale(.85)"/>
    <use href="#baya" transform="translate(268,160) scale(.8)"/>
    <use href="#venado" transform="translate(304,164) scale(.85)"/>
    <g transform="translate(58,96) scale(.85)"><use href="#pajaro" class="flota-2"/></g>
    <g transform="translate(370,132) scale(.9)"><use href="#hada" class="flota"/></g>
    <g transform="translate(180,86) scale(.95)"><use href="#mariposa" class="flota-3"/></g>
    <g transform="translate(126,72) scale(.8)"><use href="#corazon" class="flota-2"/></g>
    <g fill="#EFC15E">
      <circle class="chispa" cx="348" cy="98" r="2.6"/>
      <circle class="chispa" cx="378" cy="76" r="2.2"/>
      <circle class="chispa" cx="326" cy="70" r="2.4"/>
    </g>
  </svg>

  <p class="pie">Dos añitos · Otoño 2026</p>
</div>

<div class="hojas" id="hojas" aria-hidden="true"></div>

<script>
const DATOS = {
  nombre:        "Lilian",
  fechaHora:     "2026-10-03T15:00:00",
  duracionHoras: 4,
  lugar:         "Terraza del Coto 11, Paseo de los Parques",
  direccion:     "Av. San Blas 2285, Santa Cruz del Valle, Tlaquepaque, Jalisco",
  whatsapp:      "5213315524973",
  mensajeRSVP:   "¡Hola! Quiero confirmar mi asistencia a la fiesta de Lilian. Vamos _____ personas."
};

const $ = s => document.querySelector(s);
const f = new Date(DATOS.fechaHora);

$("#btn-whatsapp").href = "https://wa.me/" + DATOS.whatsapp + "?text=" + encodeURIComponent(DATOS.mensajeRSVP);

const zulu = d => d.toISOString().replace(/[-:]|\.\d{3}/g, "");
const fin = new Date(f.getTime() + DATOS.duracionHoras * 3600 * 1000);
$("#btn-calendario").href =
  "https://calendar.google.com/calendar/render?action=TEMPLATE" +
  "&text=" + encodeURIComponent("Cumpleaños de " + DATOS.nombre + " — 2 años") +
  "&dates=" + zulu(f) + "/" + zulu(fin) +
  "&location=" + encodeURIComponent(DATOS.lugar + ", " + DATOS.direccion);

const celdas = {
  d: document.querySelector('[data-c="d"]'),
  h: document.querySelector('[data-c="h"]'),
  m: document.querySelector('[data-c="m"]'),
  s: document.querySelector('[data-c="s"]')
};
function tic(){
  const falta = f - new Date();
  if (falta <= 0){
    $("#cuenta").innerHTML = '<p class="subtitulo" style="flex:1">¡Hoy es el día!</p>';
    return clearInterval(reloj);
  }
  const seg = Math.floor(falta / 1000);
  celdas.d.textContent = String(Math.floor(seg / 86400)).padStart(2, "0");
  celdas.h.textContent = String(Math.floor(seg % 86400 / 3600)).padStart(2, "0");
  celdas.m.textContent = String(Math.floor(seg % 3600 / 60)).padStart(2, "0");
  celdas.s.textContent = String(seg % 60).padStart(2, "0");
}
tic();
const reloj = setInterval(tic, 1000);

const ojo = new IntersectionObserver(entradas => {
  entradas.forEach(e => { if (e.isIntersecting){ e.target.classList.add("dentro"); ojo.unobserve(e.target); } });
}, {threshold:.15});
document.querySelectorAll(".rev").forEach(el => ojo.observe(el));

if (!matchMedia("(prefers-reduced-motion: reduce)").matches){
  const formas = [
    '<path d="M11,1 C19,7 19,16 11,21 C3,16 3,7 11,1 Z" fill="COLOR" stroke="#6B4A3A" stroke-width="1.6"/><path d="M11,3 V19" stroke="#6B4A3A" stroke-width="1.2"/>',
    '<path d="M2,11 C8,3 16,3 20,11 C16,19 8,19 2,11 Z" fill="COLOR" stroke="#6B4A3A" stroke-width="1.6"/><path d="M4,11 H18" stroke="#6B4A3A" stroke-width="1.2"/>',
    '<path d="M11,1 C13,6 19,5 19,9 C19,12 14,12 11,21 C8,12 3,12 3,9 C3,5 9,6 11,1 Z" fill="COLOR" stroke="#6B4A3A" stroke-width="1.5" stroke-linejoin="round"/>'
  ];
  const colores = ["#E9A9B8","#DC8A57","#EFC15E","#8A9E72","#F7D6DE"];
  const cielo = document.getElementById("hojas");
  for (let i = 0; i < 15; i++){
    const hoja = document.createElement("div");
    hoja.className = "hoja";
    hoja.style.left = (Math.random()*100).toFixed(1) + "%";
    hoja.style.animationDuration = (10 + Math.random()*11).toFixed(1) + "s";
    hoja.style.animationDelay = (-Math.random()*20).toFixed(1) + "s";
    const escala = (.6 + Math.random()*.8).toFixed(2);
    hoja.innerHTML = '<svg width="24" height="24" viewBox="0 0 22 22" style="transform:scale(' + escala + ')">' +
      formas[i % formas.length].replace(/COLOR/g, colores[i % colores.length]) + '</svg>';
    cielo.appendChild(hoja);
  }
}
</script>
</body>
</html>
