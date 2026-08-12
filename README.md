<!DOCTYPE html>
<html lang="es-MX">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>¡Lilian cumple 2!</title>
<meta property="og:title" content="¡Lilian cumple 2 años!">
<meta property="og:description" content="Sábado 3 de octubre · Una fiesta de hadas en el bosque">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@600;700;800&family=Caveat:wght@600;700&family=Nunito:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --crema:#FFF7E8;
    --durazno:#FFEBD0;
    --naranja:#E08B33;
    --naranja-osc:#C2661F;
    --rojo:#C24B3A;
    --verde:#6B8250;
    --verde-osc:#4C6039;
    --cafe:#5A3E2B;
    --dorado:#F0BE4B;
    --rosa:#E39A8E;

    --titulo:"Baloo 2", system-ui, sans-serif;
    --mano:"Caveat", cursive;
    --cuerpo:"Nunito", system-ui, sans-serif;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{-webkit-text-size-adjust:100%}
  body{
    background:#EBD9B8;
    color:var(--cafe);
    font-family:var(--cuerpo);
    font-weight:400;
    line-height:1.65;
  }
  .lienzo{
    position:relative;max-width:480px;margin:0 auto;overflow:hidden;
    background-color:var(--crema);
    background-image:
      radial-gradient(circle at 12px 12px, rgba(224,139,51,.10) 2.5px, transparent 2.6px),
      radial-gradient(circle at 36px 36px, rgba(107,130,80,.10) 2.5px, transparent 2.6px);
    background-size:48px 48px, 48px 48px;
  }
  @media (min-width:520px){
    body{padding:24px 0}
    .lienzo{box-shadow:0 16px 50px rgba(90,62,43,.3);border-radius:26px}
  }
  .sprites{position:absolute;width:0;height:0;overflow:hidden}

  /* hojas cayendo */
  .hojas{position:fixed;inset:0;pointer-events:none;z-index:6;overflow:hidden}
  .hoja{position:absolute;top:-12vh;opacity:0;animation:caer linear infinite}
  @keyframes caer{
    0%{transform:translate3d(0,-12vh,0) rotate(0deg);opacity:0}
    8%{opacity:.9}
    50%{transform:translate3d(30px,55vh,0) rotate(200deg)}
    92%{opacity:.75}
    100%{transform:translate3d(-22px,116vh,0) rotate(430deg);opacity:0}
  }

  /* ---------- guirnalda ---------- */
  .guirnalda{display:block;width:100%;height:auto;position:relative;z-index:4}

  /* ---------- portada ---------- */
  .portada{
    position:relative;padding:6px 22px 186px;text-align:center;
  }
  .portada .cielo{position:absolute;left:0;right:0;bottom:0;height:auto;width:100%;z-index:0}
  .portada .contenido{position:relative;z-index:3;padding-top:6px}

  .saludo{
    font-family:var(--mano);font-size:30px;line-height:1.1;color:var(--verde-osc);
    transform:rotate(-3deg);display:inline-block;
  }

  .cinta{
    position:relative;display:inline-block;margin:12px 0 6px;
    padding:8px 34px;background:var(--rojo);border-radius:14px;
    box-shadow:0 5px 0 rgba(0,0,0,.14);
    transform:rotate(-1.5deg);
  }
  .cinta::before,.cinta::after{
    content:"";position:absolute;top:12px;width:0;height:0;
    border-top:16px solid transparent;border-bottom:16px solid transparent;
  }
  .cinta::before{left:-18px;border-right:20px solid var(--naranja-osc);border-radius:4px}
  .cinta::after{right:-18px;border-left:20px solid var(--naranja-osc);border-radius:4px}
  .cinta h1{
    font-family:var(--titulo);font-weight:800;font-size:clamp(42px,13.5vw,60px);
    line-height:1.15;color:#FFF7E8;letter-spacing:.01em;
    text-shadow:0 3px 0 rgba(0,0,0,.16);
  }

  .insignia{
    position:relative;display:flex;flex-direction:column;align-items:center;justify-content:center;
    width:104px;height:104px;margin:16px auto 8px;border-radius:50%;
    background:var(--dorado);border:4px solid var(--cafe);
    box-shadow:0 6px 0 rgba(90,62,43,.3);transform:rotate(4deg);
  }
  .insignia b{font-family:var(--titulo);font-weight:800;font-size:52px;line-height:.85;color:var(--cafe)}
  .insignia span{font-family:var(--mano);font-size:20px;line-height:1;color:var(--cafe)}

  .fecha-portada{
    display:inline-block;margin-top:14px;padding:7px 22px;
    font-family:var(--titulo);font-weight:700;font-size:19px;line-height:1.25;color:var(--verde-osc);
    background:#FFFDF6;border:3px solid var(--cafe);border-radius:999px;
    box-shadow:0 4px 0 rgba(90,62,43,.22);transform:rotate(-1deg);
  }
  .baja{
    position:absolute;left:0;right:0;bottom:14px;z-index:4;
    font-family:var(--mano);font-size:22px;color:var(--naranja-osc);
    animation:respirar 2.6s ease-in-out infinite;
  }
  @keyframes respirar{0%,100%{transform:translateY(0);opacity:.6}50%{transform:translateY(7px);opacity:1}}

  /* ---------- tarjetas ---------- */
  .tarjeta{
    position:relative;z-index:3;margin:0 auto;max-width:400px;
    background:var(--durazno);border:3px solid var(--cafe);border-radius:28px;
    box-shadow:0 7px 0 rgba(90,62,43,.22);
    padding:30px 24px 26px;text-align:center;
  }
  .tarjeta.torcida-1{transform:rotate(-1.2deg)}
  .tarjeta.torcida-2{transform:rotate(1.2deg)}
  .tarjeta.clara{background:#FFFDF6}

  .bloque{padding:20px 22px}

  .titulo{
    font-family:var(--titulo);font-weight:700;font-size:26px;line-height:1.2;color:var(--rojo);
  }
  .subtitulo{font-family:var(--mano);font-size:26px;color:var(--verde-osc);line-height:1.15}
  .texto{font-size:15.5px;max-width:32ch;margin:10px auto 0}
  .texto b{font-weight:700;color:var(--naranja-osc)}

  .sticker{position:absolute;width:76px;height:auto;z-index:4;pointer-events:none}
  .st-sup-izq{top:-38px;left:-6px}
  .st-sup-der{top:-40px;right:-4px}
  .st-inf-der{bottom:-30px;right:-8px}
  .st-inf-izq{bottom:-32px;left:-8px}

  /* ---------- cuenta regresiva ---------- */
  .cuenta{display:flex;justify-content:center;gap:9px;margin-top:14px}
  .cuenta div{
    flex:1;max-width:76px;background:#FFFDF6;border:3px solid var(--cafe);border-radius:18px;
    padding:9px 2px 7px;box-shadow:0 4px 0 rgba(90,62,43,.2);
  }
  .cuenta b{display:block;font-family:var(--titulo);font-weight:800;font-size:28px;line-height:1;color:var(--verde-osc)}
  .cuenta span{font-family:var(--mano);font-size:17px;color:var(--naranja-osc)}

  /* ---------- fecha ---------- */
  .dia-grande{font-family:var(--titulo);font-weight:800;font-size:64px;line-height:.9;color:var(--rojo)}
  .mes{font-family:var(--titulo);font-weight:700;font-size:24px;color:var(--naranja-osc);text-transform:uppercase;letter-spacing:.08em}
  .dia-semana{font-family:var(--mano);font-size:28px;color:var(--verde-osc)}
  .hora{
    display:inline-block;margin-top:12px;padding:7px 20px;border-radius:999px;
    background:var(--verde);color:#FFF7E8;font-family:var(--titulo);font-weight:700;font-size:17px;
    box-shadow:0 4px 0 rgba(90,62,43,.25);
  }

  /* ---------- botones ---------- */
  .btn{
    display:inline-block;margin-top:18px;padding:13px 26px;border:3px solid var(--cafe);
    border-radius:999px;font-family:var(--titulo);font-weight:700;font-size:15px;
    color:var(--cafe);text-decoration:none;background:#FFFDF6;
    box-shadow:0 5px 0 rgba(90,62,43,.25);
    transition:transform .12s ease,box-shadow .12s ease,background .2s ease;
  }
  .btn:hover,.btn:focus-visible{background:var(--dorado)}
  .btn:active{transform:translateY(4px);box-shadow:0 1px 0 rgba(90,62,43,.25)}
  .btn.verde{background:var(--verde);color:#FFF7E8}
  .btn.verde:hover,.btn.verde:focus-visible{background:var(--verde-osc)}
  .btn.rojo{background:var(--rojo);color:#FFF7E8}
  .btn.rojo:hover,.btn.rojo:focus-visible{background:#A63A2C}
  a:focus-visible{outline:3px solid var(--naranja);outline-offset:3px}

  /* ---------- caminito ---------- */
  .camino{display:block;width:100%;max-width:400px;height:auto;margin:0 auto;position:relative;z-index:2}

  .cierre{text-align:center;position:relative;z-index:3;padding:26px 22px 0}
  .cierre .subtitulo{font-size:30px}
  .cierre .firma{font-family:var(--titulo);font-weight:800;font-size:48px;color:var(--rojo);line-height:1.1}

  .bosque-final{display:block;width:100%;height:auto;position:relative;z-index:2;margin-top:-6px}
  .pie{
    position:relative;z-index:3;padding:4px 24px 30px;text-align:center;
    font-family:var(--mano);font-size:20px;color:var(--verde-osc);
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

  <!-- árbol de caricatura -->
  <g id="arbolito">
    <path d="M-7,0 C-6,-22 -8,-40 -6,-56 L6,-56 C8,-40 6,-22 7,0 Z" fill="#8A5E3C" stroke="#5A3E2B" stroke-width="3" stroke-linejoin="round"/>
    <path d="M-2,-40 C-14,-46 -20,-52 -24,-60" stroke="#5A3E2B" stroke-width="4" fill="none" stroke-linecap="round"/>
    <path d="M2,-48 C12,-54 18,-60 22,-68" stroke="#5A3E2B" stroke-width="4" fill="none" stroke-linecap="round"/>
    <g stroke="#5A3E2B" stroke-width="3" stroke-linejoin="round">
      <circle cx="0" cy="-92" r="30" fill="#E08B33"/>
      <circle cx="-28" cy="-74" r="22" fill="#C24B3A"/>
      <circle cx="28" cy="-76" r="23" fill="#F0BE4B"/>
      <circle cx="-12" cy="-114" r="19" fill="#6B8250"/>
      <circle cx="16" cy="-112" r="17" fill="#E08B33"/>
    </g>
    <g fill="#FFF7E8" opacity=".5">
      <circle cx="-8" cy="-96" r="4"/><circle cx="10" cy="-84" r="3.4"/><circle cx="-24" cy="-78" r="3"/>
    </g>
  </g>

  <!-- arbusto -->
  <g id="mata">
    <path d="M-30,0 C-32,-20 -18,-30 -6,-26 C0,-38 18,-38 22,-24 C34,-24 36,-8 30,0 Z"
          fill="#6B8250" stroke="#4C6039" stroke-width="3" stroke-linejoin="round"/>
    <g fill="#F0BE4B" opacity=".8"><circle cx="-14" cy="-14" r="3.4"/><circle cx="8" cy="-18" r="3"/><circle cx="20" cy="-10" r="2.8"/></g>
  </g>

  <g id="helecho">
    <path d="M0,0 C7,-18 9,-38 5,-58" stroke="#4C6039" stroke-width="2.4" fill="none" stroke-linecap="round"/>
    <ellipse cx="4" cy="-9" rx="9" ry="3.4" fill="#6B8250" stroke="#4C6039" stroke-width="1.6" transform="rotate(18 4 -9)"/>
    <ellipse cx="6" cy="-21" rx="8" ry="3" fill="#6B8250" stroke="#4C6039" stroke-width="1.6" transform="rotate(12 6 -21)"/>
    <ellipse cx="6" cy="-33" rx="6.6" ry="2.6" fill="#6B8250" stroke="#4C6039" stroke-width="1.5" transform="rotate(6 6 -33)"/>
    <ellipse cx="1" cy="-14" rx="8" ry="3" fill="#6B8250" stroke="#4C6039" stroke-width="1.6" transform="rotate(-24 1 -14)"/>
    <ellipse cx="1" cy="-27" rx="6.6" ry="2.6" fill="#6B8250" stroke="#4C6039" stroke-width="1.5" transform="rotate(-18 1 -27)"/>
    <ellipse cx="3" cy="-40" rx="5" ry="2.2" fill="#6B8250" stroke="#4C6039" stroke-width="1.4" transform="rotate(-10 3 -40)"/>
  </g>

  <!-- hongo con carita -->
  <g id="hongo">
    <path d="M-5,0 L-4.4,-13 C-4.4,-16 4.4,-16 4.4,-13 L5,0 Z" fill="#FFF3DC" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
    <path d="M-16,-13 C-16,-30 16,-30 16,-13 Z" fill="#C24B3A" stroke="#5A3E2B" stroke-width="2.6" stroke-linejoin="round"/>
    <circle cx="-7" cy="-20" r="3" fill="#FFF7E8"/>
    <circle cx="2.5" cy="-23" r="2.4" fill="#FFF7E8"/>
    <circle cx="9" cy="-17.5" r="2" fill="#FFF7E8"/>
    <circle cx="-3.4" cy="-8" r="1.2" fill="#5A3E2B"/>
    <circle cx="3.4" cy="-8" r="1.2" fill="#5A3E2B"/>
    <path d="M-2,-5 C0,-3.4 2,-3.4 3,-5" stroke="#5A3E2B" stroke-width="1.2" fill="none" stroke-linecap="round"/>
  </g>

  <!-- venadito -->
  <g id="venado">
    <g stroke="#5A3E2B" stroke-width="2.6" stroke-linejoin="round">
      <rect x="-18" y="-27" width="8" height="29" rx="4" fill="#C98A52"/>
      <rect x="-5" y="-27" width="8" height="29" rx="4" fill="#C98A52"/>
      <rect x="8" y="-27" width="8" height="29" rx="4" fill="#D9A067"/>
      <rect x="19" y="-27" width="8" height="29" rx="4" fill="#D9A067"/>
      <ellipse cx="-24" cy="-42" rx="6.4" ry="7.4" fill="#FFF3DC"/>
      <ellipse cx="0" cy="-42" rx="26" ry="18" fill="#D9A067"/>
      <path d="M14,-52 C20,-62 24,-68 28,-74 L40,-67 C36,-61 31,-53 27,-47 Z" fill="#D9A067"/>
      <ellipse cx="38" cy="-76" rx="13" ry="11" fill="#D9A067"/>
      <ellipse cx="27" cy="-86" rx="8.4" ry="5" fill="#C07B44" transform="rotate(-30 27 -86)"/>
      <ellipse cx="44" cy="-88" rx="7.6" ry="4.4" fill="#C07B44" transform="rotate(26 44 -88)"/>
    </g>
    <ellipse cx="47" cy="-71" rx="7" ry="5.6" fill="#E8BE90"/>
    <ellipse cx="49.5" cy="-71" rx="2.6" ry="2" fill="#5A3E2B"/>
    <circle cx="39" cy="-79" r="2.6" fill="#3B2A1E"/>
    <circle cx="39.9" cy="-80" r="1" fill="#FFF"/>
    <circle cx="31" cy="-72" r="3.4" fill="#E39A8E" opacity=".55"/>
    <g fill="#FFF3DC">
      <circle cx="-8" cy="-49" r="3"/><circle cx="1" cy="-52" r="2.6"/>
      <circle cx="10" cy="-49" r="2.8"/><circle cx="-15" cy="-43" r="2.4"/><circle cx="4" cy="-44" r="2.2"/>
    </g>
  </g>

  <!-- conejito -->
  <g id="conejo">
    <g stroke="#5A3E2B" stroke-width="2.6" stroke-linejoin="round">
      <circle cx="-15" cy="-9" r="6.4" fill="#FFF3DC"/>
      <ellipse cx="0" cy="-17" rx="15" ry="17" fill="#F2E4CC"/>
      <ellipse cx="-4" cy="-52" rx="4.6" ry="13" fill="#F2E4CC" transform="rotate(-11 -4 -52)"/>
      <ellipse cx="9" cy="-53" rx="4.4" ry="13" fill="#F2E4CC" transform="rotate(10 9 -53)"/>
      <circle cx="2" cy="-37" r="12" fill="#F2E4CC"/>
      <ellipse cx="-2" cy="-2.5" rx="7" ry="3.8" fill="#FFF3DC"/>
      <ellipse cx="9" cy="-3" rx="6" ry="3.4" fill="#FFF3DC"/>
    </g>
    <ellipse cx="-4" cy="-52" rx="1.9" ry="8" fill="#E39A8E" transform="rotate(-11 -4 -52)"/>
    <ellipse cx="9" cy="-53" rx="1.8" ry="8" fill="#E39A8E" transform="rotate(10 9 -53)"/>
    <circle cx="-2.4" cy="-38.5" r="2.4" fill="#3B2A1E"/>
    <circle cx="-1.5" cy="-39.6" r=".9" fill="#FFF"/>
    <circle cx="7.6" cy="-38.5" r="2.4" fill="#3B2A1E"/>
    <circle cx="8.5" cy="-39.6" r=".9" fill="#FFF"/>
    <ellipse cx="2.6" cy="-33" r="2" rx="2.4" ry="1.8" fill="#D9756C"/>
    <circle cx="-8" cy="-33" r="3.4" fill="#E39A8E" opacity=".5"/>
    <circle cx="13" cy="-33" r="3.4" fill="#E39A8E" opacity=".5"/>
  </g>

  <!-- ardilla -->
  <g id="ardilla">
    <path d="M-8,-6 C-31,-9 -34,-46 -11,-51 C-22,-41 -24,-18 -6,-15 Z" fill="#C2702F" stroke="#5A3E2B" stroke-width="2.6" stroke-linejoin="round"/>
    <g stroke="#5A3E2B" stroke-width="2.6" stroke-linejoin="round">
      <ellipse cx="2" cy="-18" rx="13" ry="16" fill="#D08840"/>
      <circle cx="6" cy="-37" r="10.4" fill="#D08840"/>
      <ellipse cx="0.5" cy="-46" rx="3.6" ry="5.2" fill="#C2702F" transform="rotate(-16 0.5 -46)"/>
      <ellipse cx="11" cy="-46.5" rx="3.4" ry="5" fill="#C2702F" transform="rotate(14 11 -46.5)"/>
    </g>
    <ellipse cx="4" cy="-15" rx="8" ry="9.4" fill="#F2DFB8"/>
    <circle cx="9" cy="-38.5" r="2.4" fill="#3B2A1E"/>
    <circle cx="9.9" cy="-39.6" r=".9" fill="#FFF"/>
    <circle cx="2.6" cy="-38.5" r="2.2" fill="#3B2A1E"/>
    <ellipse cx="14" cy="-35" rx="2.2" ry="1.7" fill="#5A3E2B"/>
    <circle cx="0" cy="-32" r="3" fill="#E39A8E" opacity=".5"/>
    <g stroke="#5A3E2B" stroke-width="2.2" stroke-linejoin="round">
      <ellipse cx="15" cy="-22" rx="5.2" ry="6" fill="#DCA95A"/>
      <path d="M9.6,-25.6 C9.6,-30 20.4,-30 20.4,-25.6 Z" fill="#8A5E3C"/>
    </g>
  </g>

  <!-- mariposa -->
  <g id="mariposa">
    <g stroke="#5A3E2B" stroke-width="1.8" stroke-linejoin="round">
      <ellipse cx="-6.5" cy="-5" rx="7" ry="5.6" fill="#E08B33" transform="rotate(-22 -6.5 -5)"/>
      <ellipse cx="6.5" cy="-5" rx="7" ry="5.6" fill="#E08B33" transform="rotate(22 6.5 -5)"/>
      <ellipse cx="-5" cy="3.6" rx="5" ry="4.2" fill="#F0BE4B"/>
      <ellipse cx="5" cy="3.6" rx="5" ry="4.2" fill="#F0BE4B"/>
      <ellipse cx="0" cy="-0.5" rx="1.8" ry="7.4" fill="#5A3E2B"/>
    </g>
    <path d="M-0.8,-7.4 C-2.8,-10.4 -5,-11.4 -6.6,-11.8 M0.8,-7.4 C2.8,-10.4 5,-11.4 6.6,-11.8"
          stroke="#5A3E2B" stroke-width="1.4" fill="none" stroke-linecap="round"/>
    <circle cx="-6.6" cy="-12.6" r="1.4" fill="#5A3E2B"/>
    <circle cx="6.6" cy="-12.6" r="1.4" fill="#5A3E2B"/>
  </g>

  <!-- pajarito -->
  <g id="pajaro">
    <g stroke="#5A3E2B" stroke-width="2.2" stroke-linejoin="round">
      <ellipse cx="0" cy="-8" rx="11" ry="9" fill="#E39A8E"/>
      <circle cx="8" cy="-15" r="6.4" fill="#E39A8E"/>
      <path d="M-9,-10 C-16,-16 -20,-14 -22,-10 C-18,-6 -13,-5 -9,-7 Z" fill="#C77A6E"/>
    </g>
    <path d="M14,-15 l6,2 -6,2 Z" fill="#F0BE4B" stroke="#5A3E2B" stroke-width="1.6" stroke-linejoin="round"/>
    <circle cx="10" cy="-17" r="1.8" fill="#3B2A1E"/>
    <path d="M-3,0 v4 M3,0 v4" stroke="#F0BE4B" stroke-width="2.2" stroke-linecap="round"/>
  </g>

  <!-- hada -->
  <g id="hada">
    <g stroke="#5A3E2B" stroke-width="2" stroke-linejoin="round">
      <ellipse cx="-12" cy="-36" rx="10" ry="15" fill="#FFF9EC" opacity=".95" transform="rotate(-24 -12 -36)"/>
      <ellipse cx="12" cy="-36" rx="10" ry="15" fill="#FFF9EC" opacity=".95" transform="rotate(24 12 -36)"/>
      <ellipse cx="-9" cy="-20" rx="7" ry="10" fill="#FFF9EC" opacity=".95" transform="rotate(-16 -9 -20)"/>
      <ellipse cx="9" cy="-20" rx="7" ry="10" fill="#FFF9EC" opacity=".95" transform="rotate(16 9 -20)"/>
      <path d="M0,-36 C8,-25 13,-11 14,-3 L-14,-3 C-13,-11 -8,-25 0,-36 Z" fill="#F0BE4B"/>
      <circle cx="0" cy="-45" r="9" fill="#F5D7B4"/>
    </g>
    <path d="M-7,-30 C-13,-26 -15,-21 -16,-17" stroke="#F5D7B4" stroke-width="3.6" fill="none" stroke-linecap="round"/>
    <path d="M7,-30 C13,-27 16,-24 18,-21" stroke="#F5D7B4" stroke-width="3.6" fill="none" stroke-linecap="round"/>
    <path d="M-4.6,-3 L-4.6,3 M4.6,-3 L4.6,3" stroke="#F5D7B4" stroke-width="3.6" stroke-linecap="round"/>
    <path d="M-9,-45 C-9,-58 9,-58 9,-45 C7,-50 -7,-50 -9,-45 Z" fill="#8A5E3C" stroke="#5A3E2B" stroke-width="2" stroke-linejoin="round"/>
    <circle cx="-8.4" cy="-50" r="4.2" fill="#8A5E3C" stroke="#5A3E2B" stroke-width="2"/>
    <circle cx="8.4" cy="-50" r="4.2" fill="#8A5E3C" stroke="#5A3E2B" stroke-width="2"/>
    <circle cx="-3" cy="-44.5" r="1.8" fill="#3B2A1E"/>
    <circle cx="3" cy="-44.5" r="1.8" fill="#3B2A1E"/>
    <path d="M-2.6,-40 C-1,-38.4 1,-38.4 2.6,-40" stroke="#3B2A1E" stroke-width="1.3" fill="none" stroke-linecap="round"/>
    <circle cx="-6.4" cy="-41.4" r="2.2" fill="#E39A8E" opacity=".6"/>
    <circle cx="6.4" cy="-41.4" r="2.2" fill="#E39A8E" opacity=".6"/>
    <path d="M0,-56 C-5,-54 -6,-49 0,-51 C6,-49 5,-54 0,-56 Z" fill="#C24B3A" stroke="#5A3E2B" stroke-width="1.6"/>
    <path d="M18,-21 L26,-31" stroke="#8A5E3C" stroke-width="2.2" stroke-linecap="round"/>
    <path d="M26,-34 l2,3 3.4,.6 -2.4,2.6 .6,3.4 -3.6,-1.6 -3.4,1.6 .4,-3.4 -2.4,-2.6 3.4,-.6 Z"
          fill="#F0BE4B" stroke="#5A3E2B" stroke-width="1.4" stroke-linejoin="round"/>
  </g>

  <!-- hojita -->
  <g id="hojita">
    <path d="M0,-17 C8,-11 8,-2 0,3 C-8,-2 -8,-11 0,-17 Z" fill="#E08B33" stroke="#5A3E2B" stroke-width="2" stroke-linejoin="round"/>
    <path d="M0,-15 V1.5" stroke="#5A3E2B" stroke-width="1.4"/>
  </g>
  <g id="hojita-verde">
    <path d="M0,-17 C8,-11 8,-2 0,3 C-8,-2 -8,-11 0,-17 Z" fill="#6B8250" stroke="#5A3E2B" stroke-width="2" stroke-linejoin="round"/>
    <path d="M0,-15 V1.5" stroke="#5A3E2B" stroke-width="1.4"/>
  </g>
  <g id="hojita-roja">
    <path d="M0,-17 C8,-11 8,-2 0,3 C-8,-2 -8,-11 0,-17 Z" fill="#C24B3A" stroke="#5A3E2B" stroke-width="2" stroke-linejoin="round"/>
    <path d="M0,-15 V1.5" stroke="#5A3E2B" stroke-width="1.4"/>
  </g>

  <g id="bellota">
    <ellipse cx="0" cy="-5" rx="6" ry="7" fill="#DCA95A" stroke="#5A3E2B" stroke-width="2" stroke-linejoin="round"/>
    <path d="M-7.6,-10 C-7.6,-16 7.6,-16 7.6,-10 Z" fill="#8A5E3C" stroke="#5A3E2B" stroke-width="2" stroke-linejoin="round"/>
    <path d="M0,-16 V-19.6" stroke="#5A3E2B" stroke-width="2" stroke-linecap="round"/>
  </g>

  <!-- huella -->
  <g id="huella">
    <ellipse cx="0" cy="0" rx="4.4" ry="3.4" fill="#C89A5B" opacity=".55"/>
    <circle cx="-4" cy="-5" r="1.6" fill="#C89A5B" opacity=".55"/>
    <circle cx="0" cy="-6.4" r="1.6" fill="#C89A5B" opacity=".55"/>
    <circle cx="4" cy="-5" r="1.6" fill="#C89A5B" opacity=".55"/>
  </g>
</defs>
</svg>

<div class="lienzo">

  <!-- ================= GUIRNALDA ================= -->
  <svg class="guirnalda" viewBox="0 0 400 92" aria-hidden="true">
    <path d="M0,10 C70,52 150,52 200,40 C250,28 330,44 400,14" stroke="#5A3E2B" stroke-width="2.6" fill="none"/>
    <g>
      <path d="M22,26 L44,32 L34,54 Z" fill="#C24B3A" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
      <path d="M62,36 L84,42 L74,64 Z" fill="#F0BE4B" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
      <path d="M104,44 L126,48 L117,70 Z" fill="#6B8250" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
      <path d="M148,48 L170,50 L162,72 Z" fill="#E08B33" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
      <path d="M196,44 L218,42 L212,64 Z" fill="#C24B3A" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
      <path d="M240,38 L262,38 L254,60 Z" fill="#F0BE4B" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
      <path d="M282,36 L304,40 L294,62 Z" fill="#6B8250" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
      <path d="M324,30 L346,32 L338,54 Z" fill="#E08B33" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
      <path d="M366,20 L388,20 L380,42 Z" fill="#C24B3A" stroke="#5A3E2B" stroke-width="2.4" stroke-linejoin="round"/>
    </g>
    <use href="#hojita" transform="translate(46,20) rotate(20) scale(.75)"/>
    <use href="#hojita-verde" transform="translate(190,36) rotate(-12) scale(.75)"/>
    <use href="#hojita-roja" transform="translate(310,28) rotate(16) scale(.75)"/>
  </svg>

  <!-- ================= PORTADA ================= -->
  <header class="portada">
    <svg class="cielo" viewBox="0 0 400 560" preserveAspectRatio="xMidYMax meet" aria-hidden="true">
      <circle cx="200" cy="120" r="150" fill="#FFEFCE" opacity=".7"/>
      <use href="#arbolito" transform="translate(34,556) scale(1.35)"/>
      <use href="#arbolito" transform="translate(368,558) scale(1.45)"/>
      <use href="#arbolito" transform="translate(112,548) scale(.85)" opacity=".9"/>
      <use href="#arbolito" transform="translate(300,546) scale(.8)" opacity=".9"/>
      <path d="M-10,560 C90,520 300,520 410,558 L410,600 L-10,600 Z" fill="#8FA36A" stroke="#4C6039" stroke-width="3"/>
      <path d="M-10,572 C90,536 300,536 410,570" stroke="#FFF7E8" stroke-width="3" fill="none" opacity=".45"/>
      <use href="#mata" transform="translate(46,556) scale(.95)"/>
      <use href="#mata" transform="translate(356,558) scale(1)"/>
      <use href="#helecho" transform="translate(104,556) scale(1.1)"/>
      <use href="#helecho" transform="translate(292,554) scale(1.05)"/>
      <use href="#venado" transform="translate(268,552) scale(1.15)"/>
      <use href="#conejo" class="brinca" transform="translate(126,554) scale(1.05)"/>
      <use href="#ardilla" transform="translate(186,552) scale(1)"/>
      <use href="#hongo" transform="translate(222,554) scale(1.05)"/>
      <use href="#hongo" transform="translate(240,558) scale(.7)"/>
      <use href="#bellota" transform="translate(160,556) scale(.95)"/>
      <use href="#pajaro" class="flota-3" transform="translate(88,470) scale(1)"/>
      <use href="#hada" class="flota" transform="translate(318,436) scale(1.15)"/>
      <use href="#mariposa" class="flota-2" transform="translate(102,392) scale(1.2)"/>
      <use href="#mariposa" class="flota-3" transform="translate(266,346) scale(1)"/>
      <g fill="#F0BE4B">
        <circle class="chispa" cx="298" cy="392" r="3"/>
        <circle class="chispa" cx="342" cy="360" r="2.4"/>
        <circle class="chispa" cx="272" cy="440" r="2.6"/>
        <circle class="chispa" cx="128" cy="344" r="2.4"/>
        <circle class="chispa" cx="196" cy="300" r="2.2"/>
      </g>
    </svg>

    <div class="contenido">
      <p class="saludo">¡Ven al bosque a jugar!</p>
      <div class="cinta"><h1>Lilian</h1></div>
      <div class="insignia"><b>2</b><span>añitos</span></div>
      <p class="fecha-portada">Sábado 3 de octubre</p>
    </div>
    <p class="baja">↓ desliza ↓</p>
  </header>

  <!-- ================= INVITACIÓN ================= -->
  <div style="height:16px"></div>
  <section class="tarjeta torcida-1 rev">
    <svg class="sticker st-sup-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#mariposa" class="flota" transform="translate(40,52) scale(1.7)"/>
    </svg>
    <svg class="sticker st-sup-der" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#hojita-roja" transform="translate(40,56) rotate(18) scale(1.5)"/>
    </svg>
    <p class="subtitulo">Las hojas ya se pintaron de oro</p>
    <p class="texto">y eso solo puede significar una cosa: <b>¡cumplo dos años!</b> Te invito a mi fiesta entre hadas, hongos y animalitos.</p>
    <svg viewBox="0 0 300 90" style="width:100%;height:auto;margin-top:6px" aria-hidden="true">
      <use href="#conejo" class="brinca" transform="translate(96,84) scale(.95)"/>
      <use href="#ardilla" transform="translate(196,84) scale(.9)"/>
      <use href="#hongo" transform="translate(150,84) scale(.85)"/>
      <use href="#helecho" transform="translate(130,84) scale(.75)"/>
      <use href="#bellota" transform="translate(172,84) scale(.85)"/>
      <path d="M20,84 C90,74 210,74 280,84" stroke="#4C6039" stroke-width="2.2" fill="none" opacity=".45"/>
    </svg>
  </section>

  <svg class="camino" viewBox="0 0 300 44" aria-hidden="true">
    <use href="#huella" transform="translate(90,30) rotate(12)"/>
    <use href="#huella" transform="translate(118,18) rotate(12)"/>
    <use href="#huella" transform="translate(150,30) rotate(-8)"/>
    <use href="#huella" transform="translate(182,18) rotate(-8)"/>
    <use href="#huella" transform="translate(212,30) rotate(6)"/>
  </svg>

  <!-- ================= CUENTA REGRESIVA ================= -->
  <section class="tarjeta clara torcida-2 rev">
    <svg class="sticker st-sup-der" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#pajaro" class="flota-2" transform="translate(38,52) scale(1.5)"/>
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
      <use href="#hongo" transform="translate(50,70) scale(.85)"/>
    </svg>
  </section>

  <div style="height:26px"></div>

  <!-- ================= LA CITA ================= -->
  <section class="tarjeta torcida-1 rev">
    <svg class="sticker st-sup-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#hojita-verde" transform="translate(40,56) rotate(-20) scale(1.5)"/>
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
    <use href="#huella" transform="translate(152,20) rotate(8)"/>
    <use href="#huella" transform="translate(184,32) rotate(8)"/>
    <use href="#huella" transform="translate(214,20) rotate(-6)"/>
  </svg>

  <!-- ================= EL LUGAR ================= -->
  <section class="tarjeta clara torcida-2 rev">
    <svg class="sticker st-sup-der" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#mariposa" class="flota-3" transform="translate(40,52) scale(1.6)"/>
    </svg>
    <p class="titulo">Nos vemos aquí</p>
    <p class="subtitulo" style="margin-top:6px">Terraza del Coto 11<br>Paseo de los Parques</p>
    <p class="texto">Av. San Blas 2285, Santa Cruz del Valle, Tlaquepaque, Jalisco</p>
    <a class="btn verde" href="https://maps.app.goo.gl/nrrdH24tucgffceq8" target="_blank" rel="noopener">Cómo llegar</a>
    <svg class="sticker st-inf-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#conejo" class="brinca" transform="translate(38,74) scale(1)"/>
    </svg>
  </section>

  <div style="height:30px"></div>

  <!-- ================= REGALOS ================= -->
  <section class="tarjeta torcida-1 rev">
    <svg class="sticker st-sup-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#bellota" transform="translate(30,60) rotate(-14) scale(1.4)"/>
      <use href="#hojita" transform="translate(54,58) rotate(24) scale(1.1)"/>
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
    <use href="#huella" transform="translate(124,18) rotate(10)"/>
    <use href="#huella" transform="translate(156,30) rotate(-8)"/>
    <use href="#huella" transform="translate(188,18) rotate(-8)"/>
  </svg>

  <!-- ================= CONFIRMACIÓN ================= -->
  <section class="tarjeta clara torcida-2 rev">
    <svg class="sticker st-sup-der" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#hada" class="flota" transform="translate(38,68) scale(.95)"/>
    </svg>
    <p class="titulo">¿Nos acompañas?</p>
    <p class="texto">Avísanos cuántos vienen antes del <b id="limite">26 de septiembre</b> para apartar su lugar en el bosque.</p>
    <a class="btn rojo" id="btn-whatsapp" href="#" target="_blank" rel="noopener">Confirmar por WhatsApp</a>
    <svg class="sticker st-inf-izq" viewBox="0 0 80 80" aria-hidden="true">
      <use href="#hongo" transform="translate(30,68) scale(1.2)"/>
      <use href="#helecho" transform="translate(54,70) scale(.85)"/>
    </svg>
  </section>

  <!-- ================= CIERRE ================= -->
  <div class="cierre rev">
    <p class="subtitulo">¡Te espero en el bosque!</p>
    <p class="firma">Lilian</p>
  </div>

  <svg class="bosque-final" viewBox="0 0 400 180" aria-hidden="true">
    <use href="#arbolito" transform="translate(36,164) scale(1)"/>
    <use href="#arbolito" transform="translate(364,166) scale(1.05)"/>
    <use href="#arbolito" transform="translate(120,158) scale(.7)" opacity=".9"/>
    <use href="#arbolito" transform="translate(288,156) scale(.68)" opacity=".9"/>
    <path d="M-10,168 C90,138 300,138 410,166 L410,200 L-10,200 Z" fill="#8FA36A" stroke="#4C6039" stroke-width="3"/>
    <path d="M-10,178 C90,150 300,150 410,176" stroke="#FFF7E8" stroke-width="3" fill="none" opacity=".45"/>
    <use href="#mata" transform="translate(200,166) scale(.85)"/>
    <use href="#helecho" transform="translate(64,164) scale(.95)"/>
    <use href="#conejo" class="brinca" transform="translate(96,164) scale(.85)"/>
    <use href="#hongo" transform="translate(136,164) scale(.9)"/>
    <use href="#hongo" transform="translate(152,168) scale(.6)"/>
    <use href="#ardilla" transform="translate(240,164) scale(.85)"/>
    <use href="#bellota" transform="translate(268,166) scale(.9)"/>
    <use href="#venado" transform="translate(304,164) scale(.85)"/>
    <use href="#pajaro" class="flota-2" transform="translate(58,96) scale(.85)"/>
    <use href="#hada" class="flota" transform="translate(370,132) scale(.9)"/>
    <use href="#mariposa" class="flota-3" transform="translate(180,86) scale(.95)"/>
    <g fill="#F0BE4B">
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
    '<path d="M11,1 C19,7 19,16 11,21 C3,16 3,7 11,1 Z" fill="COLOR" stroke="#5A3E2B" stroke-width="1.6"/><path d="M11,3 V19" stroke="#5A3E2B" stroke-width="1.2"/>',
    '<path d="M2,11 C8,3 16,3 20,11 C16,19 8,19 2,11 Z" fill="COLOR" stroke="#5A3E2B" stroke-width="1.6"/><path d="M4,11 H18" stroke="#5A3E2B" stroke-width="1.2"/>',
    '<path d="M11,2 C17,6 19,12 11,20 C3,12 5,6 11,2 Z" fill="COLOR" stroke="#5A3E2B" stroke-width="1.6"/>'
  ];
  const colores = ["#E08B33","#C24B3A","#F0BE4B","#6B8250","#D9A067"];
  const cielo = document.getElementById("hojas");
  for (let i = 0; i < 14; i++){
    const hoja = document.createElement("div");
    hoja.className = "hoja";
    hoja.style.left = (Math.random()*100).toFixed(1) + "%";
    hoja.style.animationDuration = (10 + Math.random()*11).toFixed(1) + "s";
    hoja.style.animationDelay = (-Math.random()*20).toFixed(1) + "s";
    const escala = (.6 + Math.random()*.8).toFixed(2);
    hoja.innerHTML = '<svg width="24" height="24" viewBox="0 0 22 22" style="transform:scale(' + escala + ')">' +
      formas[i % formas.length].replace("COLOR", colores[i % colores.length]) + '</svg>';
    cielo.appendChild(hoja);
  }
}
</script>
</body>
</html>
