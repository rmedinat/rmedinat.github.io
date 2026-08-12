<html lang="es-MX">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Lilian cumple dos años</title>
<meta property="og:title" content="Lilian cumple dos años">
<meta property="og:description" content="Sábado 3 de octubre · Una fiesta de hadas en el bosque de otoño">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300&family=Jost:wght@300;400&family=Petit+Formal+Script&display=swap" rel="stylesheet">
<style>
  :root{
    --papel:#F3EADB;
    --corteza:#4A3527;
    --musgo:#55603F;
    --musgo-osc:#2F3A2A;
    --ambar:#C0762F;
    --hongo:#9E3B2C;
    --oro:#C8A24A;
    --script:"Petit Formal Script", cursive;
    --serif:"Cormorant Garamond", Georgia, serif;
    --sans:"Jost", "Helvetica Neue", Arial, sans-serif;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{-webkit-text-size-adjust:100%}
  body{
    background:#DED2BB;
    color:var(--corteza);
    font-family:var(--sans);
    font-weight:300;
    line-height:1.7;
  }
  .lienzo{
    position:relative;max-width:480px;margin:0 auto;overflow:hidden;
    background:
      radial-gradient(120% 60% at 50% 0%, #FBF5E9 0%, rgba(251,245,233,0) 60%),
      radial-gradient(90% 40% at 50% 100%, #E6D9BE 0%, rgba(230,217,190,0) 70%),
      var(--papel);
  }
  @media (min-width:520px){
    body{padding:28px 0}
    .lienzo{box-shadow:0 18px 60px rgba(47,58,42,.28)}
  }
  .grano{
    position:absolute;inset:0;pointer-events:none;z-index:5;opacity:.45;mix-blend-mode:multiply;
    background-image:url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='180' height='180'><filter id='n'><feTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='3'/><feColorMatrix type='saturate' values='0'/></filter><rect width='180' height='180' filter='url(%23n)' opacity='0.35'/></svg>");
  }
  .sprites{position:absolute;width:0;height:0;overflow:hidden}

  /* ---------- hojas ---------- */
  .hojas{position:fixed;inset:0;pointer-events:none;z-index:4;overflow:hidden}
  .hoja{position:absolute;top:-12vh;opacity:0;animation:caer linear infinite}
  @keyframes caer{
    0%{transform:translate3d(0,-12vh,0) rotate(0deg);opacity:0}
    8%{opacity:.85}
    50%{transform:translate3d(26px,55vh,0) rotate(180deg)}
    92%{opacity:.7}
    100%{transform:translate3d(-18px,116vh,0) rotate(400deg);opacity:0}
  }

  /* ---------- portada ---------- */
  .portada{
    position:relative;min-height:98svh;display:flex;flex-direction:column;
    justify-content:center;align-items:center;text-align:center;padding:60px 30px 200px;
  }
  .portada .escena{position:absolute;inset:0;width:100%;height:100%}
  .portada .contenido{position:relative;z-index:2}

  .eyebrow{font-size:10.5px;letter-spacing:.34em;text-transform:uppercase;color:var(--musgo)}
  .nombre{
    font-family:var(--script);font-weight:400;
    font-size:clamp(62px,21vw,94px);line-height:.95;color:var(--corteza);margin:16px 0 8px;
  }
  .edad{font-family:var(--serif);font-size:13px;letter-spacing:.42em;text-transform:uppercase;padding-left:.42em}
  .filete{width:56px;height:1px;background:rgba(74,53,39,.35);margin:24px auto}
  .fecha-portada{font-family:var(--serif);font-size:15px;letter-spacing:.2em;text-transform:uppercase}
  .baja{
    position:absolute;bottom:24px;left:0;right:0;z-index:3;font-size:9.5px;letter-spacing:.3em;
    text-transform:uppercase;color:var(--musgo);animation:respirar 3.4s ease-in-out infinite;
  }
  @keyframes respirar{0%,100%{transform:translateY(0);opacity:.55}50%{transform:translateY(6px);opacity:1}}

  /* ---------- secciones ---------- */
  section{position:relative;z-index:2;padding:56px 30px;text-align:center}
  .rotulo{font-size:10px;letter-spacing:.34em;text-transform:uppercase;color:var(--musgo);margin-bottom:20px}
  .verso{font-family:var(--serif);font-style:italic;font-weight:300;font-size:21px;line-height:1.55}
  .texto{font-size:14.5px;max-width:31ch;margin:0 auto}
  .vineta{display:block;margin:0 auto;width:200px;height:auto}

  .cuenta{display:flex;justify-content:center;gap:6px;margin-top:6px}
  .cuenta div{flex:1;max-width:80px}
  .cuenta b{
    display:block;font-family:var(--serif);font-weight:400;font-size:34px;line-height:1.1;
    color:var(--musgo-osc);font-variant-numeric:tabular-nums;
  }
  .cuenta span{font-size:9px;letter-spacing:.22em;text-transform:uppercase;color:var(--musgo)}

  .dia-semana{font-family:var(--serif);font-size:19px;letter-spacing:.34em;text-transform:uppercase;padding-left:.34em}
  .fecha-grid{
    display:flex;align-items:center;justify-content:center;gap:16px;margin:14px 0 6px;
    font-family:var(--serif);font-size:30px;letter-spacing:.06em;text-transform:uppercase;
  }
  .fecha-grid i{width:1px;height:30px;background:rgba(74,53,39,.3);display:inline-block}
  .hora{font-size:13px;letter-spacing:.16em;text-transform:uppercase;color:var(--musgo)}

  .btn{
    display:inline-block;margin-top:24px;padding:14px 28px;border:1px solid rgba(74,53,39,.4);
    border-radius:999px;font-size:10.5px;letter-spacing:.24em;text-transform:uppercase;
    color:var(--corteza);text-decoration:none;background:transparent;
    transition:background .35s ease,color .35s ease,border-color .35s ease;
  }
  .btn:hover,.btn:focus-visible{background:var(--musgo);border-color:var(--musgo);color:#FBF5E9}
  .btn.solido{background:var(--hongo);border-color:var(--hongo);color:#FBF5E9}
  .btn.solido:hover,.btn.solido:focus-visible{background:var(--musgo-osc);border-color:var(--musgo-osc)}
  a:focus-visible,button:focus-visible{outline:2px solid var(--ambar);outline-offset:3px}

  .detalles{list-style:none;max-width:30ch;margin:20px auto 0;text-align:left}
  .detalles li{position:relative;padding:11px 0 11px 26px;font-size:13.5px;border-top:1px solid rgba(74,53,39,.14)}
  .detalles li:first-child{border-top:0}
  .detalles li::before{
    content:"";position:absolute;left:2px;top:19px;width:9px;height:9px;
    border-radius:50% 50% 50% 0;transform:rotate(-45deg);background:var(--ambar);opacity:.75;
  }

  .cierre{padding-bottom:20px}
  .cierre .nombre{font-size:clamp(46px,15vw,64px)}
  .bosque-final{display:block;width:100%;height:auto;position:relative;z-index:2;margin-top:-10px}
  .pie{
    position:relative;z-index:2;padding:10px 30px 36px;text-align:center;font-size:9.5px;
    letter-spacing:.28em;text-transform:uppercase;color:rgba(85,96,63,.75);
  }

  .rev{opacity:0;transform:translateY(16px);transition:opacity .9s ease,transform .9s ease}
  .rev.dentro{opacity:1;transform:none}

  /* animalitos animados */
  .flota{animation:flotar 5s ease-in-out infinite;transform-box:fill-box;transform-origin:center}
  .flota-2{animation:flotar 6.4s ease-in-out infinite;animation-delay:-2s;transform-box:fill-box;transform-origin:center}
  .flota-3{animation:flotar 7.2s ease-in-out infinite;animation-delay:-3.6s;transform-box:fill-box;transform-origin:center}
  @keyframes flotar{0%,100%{transform:translateY(0) rotate(-3deg)}50%{transform:translateY(-10px) rotate(3deg)}}
  .chispa{animation:brillar 2.8s ease-in-out infinite;transform-box:fill-box;transform-origin:center}
  .chispa:nth-of-type(2n){animation-delay:-1.2s}
  .chispa:nth-of-type(3n){animation-delay:-2.1s}
  @keyframes brillar{0%,100%{opacity:.2;transform:scale(.7)}50%{opacity:1;transform:scale(1.15)}}

  @media (prefers-reduced-motion:reduce){
    .rev{opacity:1;transform:none;transition:none}
    .hoja{display:none}
    .baja,.flota,.flota-2,.flota-3,.chispa{animation:none!important}
  }
</style>
</head>
<body>

<!-- ================= SPRITES DEL BOSQUE ================= -->
<svg class="sprites" aria-hidden="true" xmlns="http://www.w3.org/2000/svg">
<defs>
  <radialGradient id="luz" cx="50%" cy="16%" r="62%">
    <stop offset="0%" stop-color="#FFF6E2" stop-opacity=".95"/>
    <stop offset="100%" stop-color="#FFF6E2" stop-opacity="0"/>
  </radialGradient>

  <!-- helecho -->
  <g id="helecho">
    <path d="M0,0 C6,-16 8,-34 4,-52" stroke="#55603F" stroke-width="1.4" fill="none" stroke-linecap="round"/>
    <ellipse cx="3" cy="-8" rx="7" ry="2.6" fill="#55603F" transform="rotate(18 3 -8)"/>
    <ellipse cx="5" cy="-18" rx="6.4" ry="2.4" fill="#55603F" transform="rotate(12 5 -18)"/>
    <ellipse cx="6" cy="-28" rx="5.6" ry="2.2" fill="#55603F" transform="rotate(6 6 -28)"/>
    <ellipse cx="5" cy="-38" rx="4.4" ry="1.8" fill="#55603F"/>
    <ellipse cx="1" cy="-12" rx="6.4" ry="2.4" fill="#55603F" transform="rotate(-24 1 -12)"/>
    <ellipse cx="1" cy="-23" rx="5.6" ry="2.2" fill="#55603F" transform="rotate(-18 1 -23)"/>
    <ellipse cx="2" cy="-33" rx="4.4" ry="1.8" fill="#55603F" transform="rotate(-12 2 -33)"/>
  </g>

  <!-- hongo -->
  <g id="hongo">
    <path d="M-3.6,0 L-3,-11 C-3,-13.4 3,-13.4 3,-11 L3.6,0 Z" fill="#EFE3CB"/>
    <path d="M-13,-11 C-13,-25 13,-25 13,-11 Z" fill="#9E3B2C"/>
    <circle cx="-6" cy="-16.5" r="2.2" fill="#F6EEE0" opacity=".9"/>
    <circle cx="2" cy="-19" r="1.7" fill="#F6EEE0" opacity=".9"/>
    <circle cx="7.5" cy="-14" r="1.4" fill="#F6EEE0" opacity=".9"/>
  </g>

  <!-- venado bebé -->
  <g id="venado">
    <rect x="-17" y="-27" width="6.4" height="28" rx="3.2" fill="#9C6B41"/>
    <rect x="-5" y="-27" width="6.4" height="28" rx="3.2" fill="#9C6B41"/>
    <rect x="8" y="-27" width="6.4" height="28" rx="3.2" fill="#B4794C"/>
    <rect x="18" y="-27" width="6.4" height="28" rx="3.2" fill="#B4794C"/>
    <ellipse cx="-23" cy="-42" rx="5.4" ry="6.4" fill="#F2E5CE"/>
    <ellipse cx="0" cy="-40" rx="24" ry="16" fill="#B4794C"/>
    <ellipse cx="2" cy="-33" rx="17" ry="8" fill="#E8D3B4" opacity=".6"/>
    <path d="M13,-48 C18,-56 22,-62 25,-67 L36,-60 C32,-55 28,-49 25,-44 Z" fill="#B4794C"/>
    <ellipse cx="33" cy="-71" rx="11" ry="9" fill="#B4794C"/>
    <ellipse cx="41.5" cy="-66.5" rx="6.2" ry="5" fill="#CE9B6D"/>
    <circle cx="44.5" cy="-66" r="1.9" fill="#4A3527"/>
    <circle cx="34" cy="-73.5" r="2" fill="#3B2A1E"/>
    <circle cx="34.7" cy="-74.3" r=".7" fill="#FFF" opacity=".9"/>
    <ellipse cx="24" cy="-80" rx="7.4" ry="4.2" fill="#A06B3F" transform="rotate(-30 24 -80)"/>
    <ellipse cx="38" cy="-82" rx="6.8" ry="3.8" fill="#A06B3F" transform="rotate(24 38 -82)"/>
    <g fill="#F6EEE0" opacity=".85">
      <circle cx="-8" cy="-46" r="2.5"/><circle cx="0" cy="-49" r="2.1"/>
      <circle cx="8" cy="-46" r="2.3"/><circle cx="-14" cy="-40" r="1.9"/>
      <circle cx="4" cy="-42" r="1.8"/>
    </g>
  </g>

  <!-- conejito -->
  <g id="conejo">
    <ellipse cx="-13" cy="-8" rx="5.4" ry="5" fill="#F5EDDD"/>
    <ellipse cx="0" cy="-15" rx="13" ry="15" fill="#EADFCB"/>
    <ellipse cx="-1" cy="-2.5" rx="6" ry="3.2" fill="#F5EDDD"/>
    <ellipse cx="8" cy="-3" rx="5" ry="3" fill="#F5EDDD"/>
    <circle cx="2" cy="-33" r="10" fill="#EADFCB"/>
    <ellipse cx="-3.5" cy="-47" rx="3.8" ry="11.5" fill="#EADFCB" transform="rotate(-11 -3.5 -47)"/>
    <ellipse cx="7.5" cy="-48" rx="3.6" ry="11.5" fill="#EADFCB" transform="rotate(10 7.5 -48)"/>
    <ellipse cx="-3.5" cy="-47" rx="1.7" ry="7.5" fill="#D8A9A2" transform="rotate(-11 -3.5 -47)"/>
    <ellipse cx="7.5" cy="-48" rx="1.6" ry="7.5" fill="#D8A9A2" transform="rotate(10 7.5 -48)"/>
    <circle cx="-1.5" cy="-34" r="1.9" fill="#3B2A1E"/>
    <circle cx="-0.9" cy="-34.8" r=".65" fill="#FFF" opacity=".9"/>
    <circle cx="7" cy="-34" r="1.9" fill="#3B2A1E"/>
    <circle cx="7.6" cy="-34.8" r=".65" fill="#FFF" opacity=".9"/>
    <ellipse cx="2.8" cy="-29.5" rx="2.1" ry="1.6" fill="#C98A86"/>
  </g>

  <!-- ardilla -->
  <g id="ardilla">
    <path d="M-7,-5 C-27,-8 -30,-40 -10,-45 C-19,-36 -21,-16 -5,-13 Z" fill="#A8622F"/>
    <path d="M-9,-9 C-22,-13 -23,-35 -11,-40" stroke="#C08552" stroke-width="3" fill="none" stroke-linecap="round" opacity=".7"/>
    <ellipse cx="2" cy="-16" rx="11" ry="14" fill="#B4794C"/>
    <ellipse cx="4" cy="-13" rx="7" ry="8.5" fill="#E8D3B4" opacity=".55"/>
    <circle cx="5" cy="-32" r="8.6" fill="#B4794C"/>
    <ellipse cx="0.5" cy="-39.5" rx="3.1" ry="4.6" fill="#A8622F" transform="rotate(-16 0.5 -39.5)"/>
    <ellipse cx="9.5" cy="-40" rx="3" ry="4.4" fill="#A8622F" transform="rotate(14 9.5 -40)"/>
    <circle cx="8" cy="-33" r="1.9" fill="#3B2A1E"/>
    <circle cx="8.6" cy="-33.8" r=".65" fill="#FFF" opacity=".9"/>
    <circle cx="12.4" cy="-30.5" r="1.5" fill="#4A3527"/>
    <ellipse cx="12" cy="-20" rx="4.4" ry="5" fill="#D2A24E"/>
    <path d="M7.6,-23.4 C7.6,-27 16.4,-27 16.4,-23.4 Z" fill="#7A5330"/>
    <ellipse cx="8" cy="-16" rx="3.4" ry="2.6" fill="#B4794C"/>
  </g>

  <!-- mariposa -->
  <g id="mariposa">
    <ellipse cx="-5.5" cy="-4" rx="6" ry="4.8" fill="#C0762F" opacity=".9" transform="rotate(-22 -5.5 -4)"/>
    <ellipse cx="5.5" cy="-4" rx="6" ry="4.8" fill="#C0762F" opacity=".9" transform="rotate(22 5.5 -4)"/>
    <ellipse cx="-4.4" cy="3.2" rx="4.4" ry="3.6" fill="#D9A441" opacity=".9"/>
    <ellipse cx="4.4" cy="3.2" rx="4.4" ry="3.6" fill="#D9A441" opacity=".9"/>
    <ellipse cx="0" cy="-0.5" rx="1.4" ry="6.6" fill="#4A3527"/>
    <path d="M-0.6,-6.4 C-2.6,-9.4 -4.6,-10.4 -6,-10.6 M0.6,-6.4 C2.6,-9.4 4.6,-10.4 6,-10.6"
          stroke="#4A3527" stroke-width="1" fill="none" stroke-linecap="round"/>
  </g>

  <!-- hada del bosque -->
  <g id="hada">
    <ellipse cx="-10" cy="-32" rx="8.5" ry="13" fill="#FBF3E4" opacity=".8" transform="rotate(-24 -10 -32)"/>
    <ellipse cx="10" cy="-32" rx="8.5" ry="13" fill="#FBF3E4" opacity=".8" transform="rotate(24 10 -32)"/>
    <ellipse cx="-8" cy="-19" rx="6" ry="8.5" fill="#FBF3E4" opacity=".65" transform="rotate(-16 -8 -19)"/>
    <ellipse cx="8" cy="-19" rx="6" ry="8.5" fill="#FBF3E4" opacity=".65" transform="rotate(16 8 -19)"/>
    <path d="M0,-32 C7,-22 11,-10 12,-3 L-12,-3 C-11,-10 -7,-22 0,-32 Z" fill="#D9A441"/>
    <path d="M-12,-3 C-8,-6 -4,-4 0,-6 C4,-4 8,-6 12,-3 Z" fill="#C8A24A"/>
    <path d="M-6,-30 C-11,-26 -13,-22 -14,-18" stroke="#F0D6B8" stroke-width="3.2" fill="none" stroke-linecap="round"/>
    <path d="M6,-30 C11,-27 14,-24 16,-21" stroke="#F0D6B8" stroke-width="3.2" fill="none" stroke-linecap="round"/>
    <path d="M-4,-3 L-4,3 M4,-3 L4,3" stroke="#F0D6B8" stroke-width="3.2" stroke-linecap="round"/>
    <circle cx="0" cy="-40" r="7.6" fill="#F0D6B8"/>
    <path d="M-7.6,-40 C-7.6,-51 7.6,-51 7.6,-40 C6,-44 -6,-44 -7.6,-40 Z" fill="#8A5A34"/>
    <circle cx="-7.2" cy="-44.6" r="3.4" fill="#8A5A34"/>
    <circle cx="7.2" cy="-44.6" r="3.4" fill="#8A5A34"/>
    <circle cx="-2.6" cy="-39.5" r="1.5" fill="#3B2A1E"/>
    <circle cx="2.6" cy="-39.5" r="1.5" fill="#3B2A1E"/>
    <path d="M-2.4,-35.6 C-1,-34.2 1,-34.2 2.4,-35.6" stroke="#3B2A1E" stroke-width="1" fill="none" stroke-linecap="round"/>
    <circle cx="-5.6" cy="-36.6" r="1.7" fill="#D98F7E" opacity=".5"/>
    <circle cx="5.6" cy="-36.6" r="1.7" fill="#D98F7E" opacity=".5"/>
    <path d="M0,-50 C-4,-48 -5,-44 0,-46 C5,-44 4,-48 0,-50 Z" fill="#C0762F" opacity=".9"/>
    <path d="M16,-21 L23,-30" stroke="#8A6A3A" stroke-width="1.4" stroke-linecap="round"/>
    <path d="M23,-33 l1.6,2.6 2.8,.6 -2,2.2 .4,2.8 -2.8,-1.3 -2.8,1.3 .4,-2.8 -2,-2.2 2.8,-.6 Z" fill="#E4C168"/>
  </g>

  <!-- hojita -->
  <g id="hojita">
    <path d="M0,-16 C7,-11 7,-3 0,2 C-7,-3 -7,-11 0,-16 Z" fill="#C0762F"/>
    <path d="M0,-16 V2" stroke="#4A3527" stroke-width=".8" opacity=".45"/>
  </g>

  <!-- bellota -->
  <g id="bellota">
    <ellipse cx="0" cy="-4" rx="5" ry="6" fill="#C89A5B"/>
    <path d="M-6.4,-8.6 C-6.4,-13.4 6.4,-13.4 6.4,-8.6 Z" fill="#7A5330"/>
    <path d="M0,-13.4 V-16.4" stroke="#7A5330" stroke-width="1.4" stroke-linecap="round"/>
  </g>
</defs>
</svg>

<div class="lienzo">
  <div class="grano" aria-hidden="true"></div>

  <!-- ================= PORTADA ================= -->
  <header class="portada">
    <svg class="escena" viewBox="0 0 400 640" preserveAspectRatio="xMidYMid slice" aria-hidden="true">
      <rect width="400" height="640" fill="url(#luz)"/>

      <!-- follaje -->
      <g opacity=".8" transform="translate(-16,-18) scale(.86)">
        <g fill="#C0762F">
          <circle cx="8" cy="14" r="60"/>
          <circle cx="64" cy="2" r="48"/>
          <circle cx="16" cy="72" r="46"/>
          <circle cx="76" cy="54" r="38"/>
          <circle cx="120" cy="26" r="30"/>
          <circle cx="108" cy="80" r="22"/>
        </g>
        <g fill="#9E3B2C" opacity=".26">
          <circle cx="30" cy="40" r="26"/>
          <circle cx="88" cy="28" r="20"/>
          <circle cx="48" cy="86" r="18"/>
        </g>
        <g fill="#55603F" opacity=".3">
          <circle cx="4" cy="98" r="28"/>
          <circle cx="94" cy="86" r="16"/>
          <circle cx="126" cy="46" r="13"/>
        </g>
        <g fill="#D9B25E" opacity=".34">
          <circle cx="46" cy="8" r="22"/>
          <circle cx="100" cy="54" r="14"/>
          <circle cx="20" cy="58" r="16"/>
        </g>
        <g>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(145,59) rotate(-47) scale(0.94)" fill="#B4794C"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(135,90) rotate(121) scale(0.80)" fill="#9E3B2C"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(108,119) rotate(15) scale(0.92)" fill="#55603F"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(80,122) rotate(49) scale(1.05)" fill="#B4794C"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(43,114) rotate(100) scale(0.76)" fill="#B4794C"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(5,135) rotate(116) scale(0.81)" fill="#B4794C"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(153,25) rotate(77) scale(1.07)" fill="#55603F"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(123,-5) rotate(167) scale(0.75)" fill="#C8A24A"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(59,-42) rotate(-102) scale(1.09)" fill="#55603F"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(-3,-26) rotate(-28) scale(1.03)" fill="#B4794C"/>
        </g>
      </g>
      <g opacity=".8" transform="translate(416,-18) scale(-.86,.86)">
        <g fill="#C0762F">
          <circle cx="8" cy="14" r="60"/>
          <circle cx="64" cy="2" r="48"/>
          <circle cx="16" cy="72" r="46"/>
          <circle cx="76" cy="54" r="38"/>
          <circle cx="120" cy="26" r="30"/>
          <circle cx="108" cy="80" r="22"/>
        </g>
        <g fill="#9E3B2C" opacity=".26">
          <circle cx="30" cy="40" r="26"/>
          <circle cx="88" cy="28" r="20"/>
          <circle cx="48" cy="86" r="18"/>
        </g>
        <g fill="#55603F" opacity=".3">
          <circle cx="4" cy="98" r="28"/>
          <circle cx="94" cy="86" r="16"/>
          <circle cx="126" cy="46" r="13"/>
        </g>
        <g fill="#D9B25E" opacity=".34">
          <circle cx="46" cy="8" r="22"/>
          <circle cx="100" cy="54" r="14"/>
          <circle cx="20" cy="58" r="16"/>
        </g>
        <g>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(146,59) rotate(30) scale(1.06)" fill="#C0762F"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(144,102) rotate(62) scale(0.77)" fill="#C8A24A"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(118,121) rotate(25) scale(0.99)" fill="#9E3B2C"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(80,132) rotate(-84) scale(0.75)" fill="#55603F"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(48,126) rotate(-148) scale(1.02)" fill="#55603F"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(15,126) rotate(-26) scale(0.87)" fill="#C0762F"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(145,21) rotate(-164) scale(0.99)" fill="#C8A24A"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(121,-1) rotate(-80) scale(0.79)" fill="#C0762F"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(62,-43) rotate(36) scale(0.71)" fill="#9E3B2C"/>
          <path d="M0,-14 C6.6,-9.4 6.6,-2 0,2.4 C-6.6,-2 -6.6,-9.4 0,-14 Z" transform="translate(-0,-33) rotate(-85) scale(0.98)" fill="#C8A24A"/>
        </g>
      </g>

      <!-- troncos -->
      <g stroke="#6B4B33" fill="none" stroke-linecap="round" opacity=".45">
        <path d="M34,0 C46,120 30,260 44,470" stroke-width="13"/>
        <path d="M40,132 C62,138 74,120 84,102" stroke-width="4"/>
        <path d="M36,214 C18,212 10,196 4,180" stroke-width="3.4"/>
        <path d="M366,0 C352,140 372,290 356,478" stroke-width="15"/>
        <path d="M360,120 C336,128 322,110 312,90" stroke-width="4.4"/>
        <path d="M364,232 C382,230 392,214 398,198" stroke-width="3"/>
      </g>
      <g stroke="#4A3527" stroke-width="1.6" opacity=".22" stroke-linecap="round">
        <path d="M30,60 h7"/><path d="M32,96 h5"/><path d="M31,150 h8"/><path d="M36,206 h6"/><path d="M38,286 h7"/>
        <path d="M362,72 h7"/><path d="M364,118 h6"/><path d="M366,182 h8"/><path d="M364,252 h5"/><path d="M360,330 h7"/>
      </g>

      <!-- suelo -->
      <path d="M-10,606 C70,584 150,580 200,586 C260,592 330,588 410,600 L410,660 L-10,660 Z"
            fill="#A3A06E" opacity=".62"/>
      <path d="M-10,620 C60,600 140,596 210,602 C280,608 350,604 410,614 L410,660 L-10,660 Z"
            fill="#7E8752" opacity=".7"/>
      <path d="M-10,606 C70,584 150,580 200,586 C260,592 330,588 410,600"
            stroke="#55603F" stroke-width="1.4" fill="none" opacity=".5"/>
      <path d="M116,600 C140,592 168,592 190,598" stroke="#C0762F" stroke-width="3" fill="none" opacity=".45" stroke-linecap="round"/>
      <path d="M242,596 C264,590 288,590 306,596" stroke="#9E3B2C" stroke-width="3" fill="none" opacity=".4" stroke-linecap="round"/>

      <!-- helechos -->
      <use href="#helecho" transform="translate(96,612) scale(1.15)"/>
      <use href="#helecho" transform="translate(126,618) scale(.9)"/>
      <use href="#helecho" transform="translate(268,614) scale(1.05)"/>
      <use href="#helecho" transform="translate(318,620) scale(1.25)"/>

      <!-- animalitos del bosque -->
      <use href="#venado" transform="translate(292,608) scale(1.05)"/>
      <use href="#conejo" transform="translate(112,616) scale(1)"/>
      <use href="#ardilla" transform="translate(176,614) scale(.95)"/>
      <use href="#hongo" transform="translate(214,616) scale(1)"/>
      <use href="#hongo" transform="translate(232,620) scale(.68)"/>
      <use href="#hongo" transform="translate(146,618) scale(.6)"/>
      <use href="#bellota" transform="translate(250,618) scale(1)"/>

      <!-- hada -->
      <g transform="translate(310,286) scale(1.6)"><use href="#hada" class="flota"/></g>

      <!-- mariposas -->
      <g transform="translate(96,338) scale(1.15)"><use href="#mariposa" class="flota-2"/></g>
      <g transform="translate(140,436) scale(.9)"><use href="#mariposa" class="flota-3"/></g>
      <g transform="translate(288,470) scale(1)"><use href="#mariposa" class="flota"/></g>

      <!-- polvo de hada -->
      <g fill="#E4C168">
        <circle class="chispa" cx="296" cy="252" r="2.4"/>
        <circle class="chispa" cx="340" cy="222" r="1.8"/>
        <circle class="chispa" cx="272" cy="330" r="2"/>
        <circle class="chispa" cx="118" cy="286" r="1.9"/>
        <circle class="chispa" cx="82" cy="420" r="1.7"/>
        <circle class="chispa" cx="330" cy="392" r="2.2"/>
        <circle class="chispa" cx="196" cy="196" r="1.6"/>
        <circle class="chispa" cx="256" cy="244" r="1.8"/>
        <circle class="chispa" cx="352" cy="286" r="2.1"/>
        <circle class="chispa" cx="238" cy="192" r="1.5"/>
        <circle class="chispa" cx="152" cy="234" r="1.7"/>
        <circle class="chispa" cx="304" cy="196" r="1.9"/>
      </g>
    </svg>

    <div class="contenido">
      <p class="eyebrow">El bosque se viste de otoño</p>
      <h1 class="nombre">Lilian</h1>
      <p class="edad">Cumple dos años</p>
      <div class="filete"></div>
      <p class="fecha-portada">Sábado 3 de octubre</p>
    </div>

    <p class="baja">Desliza</p>
  </header>

  <!-- ================= VERSO ================= -->
  <section class="rev">
    <p class="verso">Cuando las hojas se pintan de oro,<br>el bosque hace fiesta.</p>
    <p class="texto" style="margin-top:18px">Cumplo dos años y quiero celebrarlo entre hadas, hongos y animalitos. Ven a jugar conmigo.</p>
    <svg class="vineta" viewBox="0 0 200 70" style="margin-top:22px" aria-hidden="true">
      <g transform="translate(70,34) scale(1.3)"><use href="#mariposa" class="flota"/></g>
      <g transform="translate(104,26) scale(1)"><use href="#mariposa" class="flota-2"/></g>
      <g transform="translate(132,40) scale(.85)"><use href="#mariposa" class="flota-3"/></g>
    </svg>
  </section>

  <!-- ================= CUENTA REGRESIVA ================= -->
  <section class="rev">
    <p class="rotulo">Faltan</p>
    <div class="cuenta" id="cuenta">
      <div><b data-c="d">00</b><span>Días</span></div>
      <div><b data-c="h">00</b><span>Horas</span></div>
      <div><b data-c="m">00</b><span>Min</span></div>
      <div><b data-c="s">00</b><span>Seg</span></div>
    </div>
    <svg class="vineta" viewBox="0 0 200 70" style="margin-top:14px" aria-hidden="true">
      <path d="M28,62 C70,54 130,54 172,62" stroke="#55603F" stroke-width="1" fill="none" opacity=".3"/>
      <use href="#ardilla" transform="translate(92,62) scale(.95)"/>
      <use href="#hongo" transform="translate(126,62) scale(.8)"/>
      <use href="#helecho" transform="translate(62,62) scale(.8)"/>
      <use href="#bellota" transform="translate(140,62) scale(.9)"/>
      <g fill="#E4C168"><circle class="chispa" cx="52" cy="18" r="1.7"/><circle class="chispa" cx="164" cy="26" r="1.5"/></g>
    </svg>
  </section>

  <!-- ================= LA CITA ================= -->
  <section class="rev">
    <p class="rotulo">La cita</p>
    <p class="dia-semana">Sábado</p>
    <p class="fecha-grid"><span>03</span><i></i><span>Oct</span><i></i><span>26</span></p>
    <p class="hora">3:00 de la tarde</p>
    <a class="btn" id="btn-calendario" href="#" target="_blank" rel="noopener">Agendar el día</a>
    <svg class="vineta" viewBox="0 0 200 86" style="margin-top:12px" aria-hidden="true">
      <path d="M24,78 C70,68 132,68 176,78" stroke="#55603F" stroke-width="1" fill="none" opacity=".3"/>
      <g transform="translate(100,74) scale(1.15)"><use href="#hada" class="flota"/></g>
      <use href="#helecho" transform="translate(58,78) scale(.75)"/>
      <use href="#hongo" transform="translate(140,78) scale(.8)"/>
      <g fill="#E4C168">
        <circle class="chispa" cx="128" cy="28" r="2"/><circle class="chispa" cx="146" cy="44" r="1.6"/>
        <circle class="chispa" cx="66" cy="34" r="1.7"/><circle class="chispa" cx="82" cy="18" r="1.4"/>
      </g>
    </svg>
  </section>

  <!-- ================= EL LUGAR ================= -->
  <section class="rev">
    <p class="rotulo">El lugar</p>
    <p class="verso">Terraza del Coto 11<br>Paseo de los Parques</p>
    <p class="texto" style="margin-top:12px">Av. San Blas 2285, Santa Cruz del Valle,<br>Tlaquepaque, Jalisco</p>
    <a class="btn" href="https://maps.app.goo.gl/nrrdH24tucgffceq8" target="_blank" rel="noopener">Cómo llegar</a>
    <svg class="vineta" viewBox="0 0 200 70" style="margin-top:26px" aria-hidden="true">
      <path d="M24,62 C70,54 132,54 176,62" stroke="#55603F" stroke-width="1" fill="none" opacity=".3"/>
      <use href="#conejo" transform="translate(86,62) scale(.9)"/>
      <use href="#hongo" transform="translate(116,62) scale(.85)"/>
      <use href="#hongo" transform="translate(130,64) scale(.55)"/>
      <use href="#helecho" transform="translate(60,62) scale(.75)"/>
      <g transform="translate(146,32) scale(.9)"><use href="#mariposa" class="flota-2"/></g>
    </svg>
  </section>

  <!-- ================= REGALOS ================= -->
  <section class="rev">
    <p class="rotulo">Regalos</p>
    <p class="texto">Tu presencia es nuestro mejor regalo. Esta lista es solo una guía de opciones si deseas tener un detalle con Lilian. ¡Gracias por tu cariño! ✨🤍</p>
    <a class="btn" href="https://www.amazon.com.mx/hz/wishlist/ls/1FPXL1FS1TXNE?ref_=wl_share" target="_blank" rel="noopener">Ver lista en Amazon</a>
    <svg class="vineta" viewBox="0 0 200 100" style="margin-top:22px" aria-hidden="true">
      <path d="M20,92 C70,84 132,84 180,92" stroke="#55603F" stroke-width="1" fill="none" opacity=".3"/>
      <use href="#venado" transform="translate(104,92) scale(.9)"/>
      <use href="#helecho" transform="translate(56,92) scale(.85)"/>
      <use href="#hongo" transform="translate(148,92) scale(.8)"/>
      <g transform="translate(48,44) scale(.85)"><use href="#mariposa" class="flota-3"/></g>
    </svg>
  </section>

  <!-- ================= CONFIRMACIÓN ================= -->
  <section class="rev">
    <p class="rotulo">Confirma tu asistencia</p>
    <p class="texto">Avísanos antes del <span id="limite">26 de septiembre</span> para apartar su lugar en el bosque.</p>
    <a class="btn solido" id="btn-whatsapp" href="#" target="_blank" rel="noopener">Confirmar por WhatsApp</a>
  </section>

  <!-- ================= CIERRE ================= -->
  <section class="cierre rev">
    <p class="eyebrow">Te espero</p>
    <p class="nombre">Lilian</p>
  </section>

  <svg class="bosque-final" viewBox="0 0 400 150" aria-hidden="true">
    <path d="M-10,118 C70,100 150,96 200,102 C260,109 330,104 410,114 L410,170 L-10,170 Z"
          fill="#A3A06E" opacity=".62"/>
    <path d="M-10,132 C60,114 140,110 210,116 C280,122 350,118 410,128 L410,170 L-10,170 Z"
          fill="#7E8752" opacity=".7"/>
    <path d="M10,132 C110,118 290,118 390,132" stroke="#55603F" stroke-width="1.2" fill="none" opacity=".3"/>
    <use href="#helecho" transform="translate(26,132) scale(1)"/>
    <use href="#conejo" transform="translate(64,132) scale(.85)"/>
    <use href="#hongo" transform="translate(102,132) scale(.85)"/>
    <use href="#hongo" transform="translate(116,134) scale(.55)"/>
    <use href="#ardilla" transform="translate(150,132) scale(.85)"/>
    <use href="#bellota" transform="translate(178,133) scale(.9)"/>
    <use href="#venado" transform="translate(236,132) scale(.85)"/>
    <use href="#helecho" transform="translate(300,132) scale(.9)"/>
    <use href="#hongo" transform="translate(330,132) scale(.7)"/>
    <g transform="translate(368,110) scale(.95)"><use href="#hada" class="flota"/></g>
    <g transform="translate(196,62) scale(.9)"><use href="#mariposa" class="flota-2"/></g>
    <g transform="translate(288,48) scale(.8)"><use href="#mariposa" class="flota-3"/></g>
    <g fill="#E4C168">
      <circle class="chispa" cx="352" cy="70" r="2"/>
      <circle class="chispa" cx="378" cy="52" r="1.6"/>
      <circle class="chispa" cx="330" cy="44" r="1.8"/>
      <circle class="chispa" cx="300" cy="72" r="1.6"/>
      <circle class="chispa" cx="252" cy="52" r="1.5"/>
      <circle class="chispa" cx="150" cy="40" r="1.7"/>
      <circle class="chispa" cx="96" cy="60" r="1.5"/>
    </g>
  </svg>

  <p class="pie">Dos años · Otoño 2026</p>
</div>

<div class="hojas" id="hojas" aria-hidden="true"></div>

<script>
/* =========================================================
   DATOS DE LA FIESTA
   ========================================================= */
const DATOS = {
  nombre:        "Lilian",
  fechaHora:     "2026-10-03T15:00:00",
  duracionHoras: 4,
  lugar:         "Terraza del Coto 11, Paseo de los Parques",
  direccion:     "Av. San Blas 2285, Santa Cruz del Valle, Tlaquepaque, Jalisco",
  whatsapp:      "5213315524973",
  mensajeRSVP:   "¡Hola! Quiero confirmar mi asistencia a la fiesta de Lilian."
};

const $ = s => document.querySelector(s);
const f = new Date(DATOS.fechaHora);

$("#btn-whatsapp").href = "https://wa.me/" + DATOS.whatsapp +
  "?text=" + encodeURIComponent(DATOS.mensajeRSVP);

const zulu = d => d.toISOString().replace(/[-:]|\.\d{3}/g, "");
const fin = new Date(f.getTime() + DATOS.duracionHoras * 3600 * 1000);
$("#btn-calendario").href =
  "https://calendar.google.com/calendar/render?action=TEMPLATE" +
  "&text=" + encodeURIComponent("Cumpleaños de " + DATOS.nombre + " — 2 años") +
  "&dates=" + zulu(f) + "/" + zulu(fin) +
  "&location=" + encodeURIComponent(DATOS.lugar + ", " + DATOS.direccion);

/* cuenta regresiva */
const celdas = {
  d: document.querySelector('[data-c="d"]'),
  h: document.querySelector('[data-c="h"]'),
  m: document.querySelector('[data-c="m"]'),
  s: document.querySelector('[data-c="s"]')
};
function tic(){
  const falta = f - new Date();
  if (falta <= 0){
    $("#cuenta").innerHTML = '<p class="verso" style="flex:1">Hoy es el día</p>';
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

/* aparición al hacer scroll */
const ojo = new IntersectionObserver(entradas => {
  entradas.forEach(e => { if (e.isIntersecting){ e.target.classList.add("dentro"); ojo.unobserve(e.target); } });
}, {threshold:.18});
document.querySelectorAll(".rev").forEach(el => ojo.observe(el));

/* hojas cayendo */
if (!matchMedia("(prefers-reduced-motion: reduce)").matches){
  const formas = [
    '<path d="M11,1 C19,7 19,15 11,21 C3,15 3,7 11,1 Z" fill="COLOR"/><path d="M11,1 V21" stroke="#4A3527" stroke-width=".8" opacity=".4"/>',
    '<path d="M2,11 C8,3 16,3 20,11 C16,19 8,19 2,11 Z" fill="COLOR"/><path d="M2,11 H20" stroke="#4A3527" stroke-width=".8" opacity=".35"/>',
    '<path d="M11,2 C16,6 18,12 11,20 C4,12 6,6 11,2 Z" fill="COLOR"/>'
  ];
  const colores = ["#C0762F","#9E3B2C","#C8A24A","#8A6A2F","#7A6B3A"];
  const cielo = document.getElementById("hojas");
  for (let i = 0; i < 11; i++){
    const hoja = document.createElement("div");
    hoja.className = "hoja";
    hoja.style.left = (Math.random()*100).toFixed(1) + "%";
    hoja.style.animationDuration = (11 + Math.random()*12).toFixed(1) + "s";
    hoja.style.animationDelay = (-Math.random()*20).toFixed(1) + "s";
    const escala = (.55 + Math.random()*.7).toFixed(2);
    hoja.innerHTML = '<svg width="22" height="22" viewBox="0 0 22 22" style="transform:scale(' + escala + ')">' +
      formas[i % formas.length].replace("COLOR", colores[i % colores.length]) + '</svg>';
    cielo.appendChild(hoja);
  }
}
</script>
</body>
</html>
