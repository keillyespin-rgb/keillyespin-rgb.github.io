# keillyespin-rgb.github.io
Carta R
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Te amo plecioso ❤️</title>

<style>

/* =========================
   FUENTES
========================= */

@import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;500;600&display=swap');


/* =========================
   CONFIGURACIÓN GENERAL
========================= */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {

    min-height: 100vh;

    overflow-x: hidden;

    display: flex;

    justify-content: center;
    align-items: center;

    font-family: 'Poppins', sans-serif;

    background:
        radial-gradient(
            circle at center,
            #fff0f5 0%,
            #ffd8e5 45%,
            #f6a8bf 100%
        );

    color: #7d1835;
}


/* =========================
   CORAZONES DEL FONDO
========================= */

.corazones {

    position: fixed;

    inset: 0;

    overflow: hidden;

    pointer-events: none;

    z-index: 1;
}


.corazon {

    position: absolute;

    bottom: -50px;

    color: #e83e6f;

    animation: flotar linear infinite;

    opacity: .65;
}


@keyframes flotar {

    0% {

        transform:
            translateY(0)
            rotate(0deg)
            scale(.8);

        opacity: 0;

    }

    10% {

        opacity: .7;

    }

    50% {

        opacity: .9;

    }

    100% {

        transform:
            translateY(-110vh)
            rotate(360deg)
            scale(1.4);

        opacity: 0;

    }

}


/* =========================
   CONTENEDOR PRINCIPAL
========================= */

.contenedor {

    position: relative;

    z-index: 5;

    width: 100%;

    max-width: 600px;

    text-align: center;

    padding: 25px;

}


/* =========================
   TÍTULO
========================= */

.titulo {

    margin-bottom: 35px;

}


.titulo h1 {

    font-family: 'Great Vibes', cursive;

    font-size: clamp(
        3.5rem,
        13vw,
        6rem
    );

    font-weight: 400;

    color: #a71945;

    text-shadow:
        0 4px 15px rgba(150,20,60,.15);

}


.titulo p {

    margin-top: -10px;

    font-size: 11px;

    letter-spacing: 5px;

    color: #9b6876;

}


/* =========================
   SOBRE
========================= */

.sobre {

    position: relative;

    width: min(88vw, 400px);

    height: 260px;

    margin: auto;

    cursor: pointer;

    perspective: 1000px;

}


/* Cuerpo del sobre */

.cuerpo {

    position: absolute;

    inset: 0;

    background:
        linear-gradient(
            145deg,
            #ffd6e2,
            #f4a9bd
        );

    border-radius: 8px;

    box-shadow:
        0 20px 50px
        rgba(120,20,55,.25);

    overflow: hidden;

}


/* Parte interior del sobre */

.cuerpo::after {

    content: "";

    position: absolute;

    inset: 0;

    background: #f8bfd0;

    clip-path:
        polygon(
            0 0,
            50% 55%,
            100% 0,
            100% 100%,
            0 100%
        );

}


/* =========================
   CARTA DENTRO DEL SOBRE
========================= */

.mini-carta {

    position: absolute;

    z-index: 2;

    width: 82%;

    height: 185px;

    left: 9%;

    top: 20px;

    background: #fffafa;

    border-radius: 8px;

    padding: 25px;

    box-shadow:
        0 5px 20px
        rgba(100,20,40,.12);

    transition:
        transform 1s ease;

}


.mini-carta h2 {

    font-family: 'Great Vibes', cursive;

    font-size: 34px;

    color: #ad2048;

}


.mini-carta p {

    margin-top: 10px;

    font-size: 12px;

    color: #777;

}


/* =========================
   TAPA DEL SOBRE
========================= */

.tapa {

    position: absolute;

    z-index: 5;

    inset: 0;

    background: #f5b5c8;

    clip-path:
        polygon(
            0 0,
            100% 0,
            50% 58%
        );

    transform-origin: top;

    transition:
        transform 1s ease;

}


/* =========================
   CORAZÓN DEL SOBRE
========================= */

.corazon-centro {

    position: absolute;

    z-index: 10;

    left: 50%;

    top: 50%;

    transform:
        translate(-50%, -50%);

    font-size: 48px;

    color: #d92e5c;

    transition: .5s;

    filter:
        drop-shadow(
            0 5px 8px
            rgba(120,0,30,.2)
        );

}


/* =========================
   SOBRE ABIERTO
========================= */

.sobre.abierto .tapa {

    transform:
        rotateX(180deg);

}


.sobre.abierto .mini-carta {

    transform:
        translateY(-140px);

}


.sobre.abierto .corazon-centro {

    opacity: 0;

}


/* =========================
   TEXTO INFERIOR
========================= */

.instruccion {

    margin-top: 35px;

    font-family:
        'Great Vibes',
        cursive;

    font-size: 23px;

    color: #8f4055;

}


/* =========================
   CARTA COMPLETA
========================= */

.carta-final {

    position: fixed;

    z-index: 100;

    inset: 0;

    padding: 25px;

    display: flex;

    justify-content: center;

    align-items: center;

    background:
        rgba(
            255,
            226,
            235,
            .96
        );

    opacity: 0;

    visibility: hidden;

    transition: .8s;

}


.carta-final.mostrar {

    opacity: 1;

    visibility: visible;

}


/* =========================
   PAPEL
========================= */

.papel {

    position: relative;

    width: min(92vw, 600px);

    max-height: 85vh;

    overflow-y: auto;

    padding: 45px 32px;

    background:
        linear-gradient(
            135deg,
            #fffdfb,
            #fff5f6
        );

    border-radius: 18px;

    box-shadow:
        0 25px 70px
        rgba(100,20,45,.25);

    animation:
        aparecer .9s ease;

}


/* Animación de aparición */

@keyframes aparecer {

    from {

        transform:
            translateY(80px)
            scale(.85);

        opacity: 0;

    }

    to {

        transform:
            translateY(0)
            scale(1);

        opacity: 1;

    }

}


/* =========================
   CORAZÓN DECORATIVO
========================= */

.decoracion {

    font-size: 35px;

    margin-bottom: 10px;

}


/* =========================
   TÍTULO CARTA
========================= */

.papel h2 {

    font-family:
        'Great Vibes',
        cursive;

    font-size:
        clamp(
            3rem,
            12vw,
            5rem
        );

    font-weight: 400;

    color: #a71945;

    margin-bottom: 5px;

}


/* =========================
   TEXTO DE LA CARTA
========================= */

.texto {

    margin-top: 25px;

    text-align: left;

}


.texto p {

    font-size: 15px;

    line-height: 2;

    color: #633844;

    margin-bottom: 18px;

}


/* Palabras especiales */

.texto .amor {

    color: #d42e5d;

    font-weight: 600;

}


/* =========================
   FIRMA
========================= */

.firma {

    margin-top: 30px;

    text-align: right;

    font-family:
        'Great Vibes',
        cursive;

    font-size: 35px;

    color: #a71945;

}


/* =========================
   BOTÓN
========================= */

.boton {

    margin-top: 30px;

    padding:
        12px 28px;

    border: none;

    border-radius: 30px;

    background:
        linear-gradient(
            135deg,
            #d92e5c,
            #a71945
        );

    color: white;

    font-family:
        'Poppins',
        sans-serif;

    cursor: pointer;

    box-shadow:
        0 8px 20px
        rgba(150,20,60,.25);

}


/* =========================
   CELULAR
========================= */

@media(max-width:500px) {

    .sobre {

        height: 220px;

    }

    .mini-carta {

        height: 160px;

        padding: 18px;

    }

    .mini-carta h2 {

        font-size: 28px;

    }

    .papel {

        padding:
            35px 22px;

    }

    .texto p {

        font-size: 14px;

    }

}

</style>
</head>


<body>


<!-- ==================================
     CORAZONES
================================== -->

<div class="corazones">

    <span class="corazon"
          style="left:5%; font-size:22px; animation-duration:8s;">
        ❤️
    </span>

    <span class="corazon"
          style="left:15%; font-size:30px; animation-duration:11s; animation-delay:2s;">
        💗
    </span>

    <span class="corazon"
          style="left:28%; font-size:18px; animation-duration:7s; animation-delay:1s;">
        💕
    </span>

    <span class="corazon"
          style="left:42%; font-size:35px; animation-duration:10s; animation-delay:3s;">
        ❤️
    </span>

    <span class="corazon"
          style="left:58%; font-size:20px; animation-duration:8s; animation-delay:2s;">
        💕
    </span>

    <span class="corazon"
          style="left:70%; font-size:32px; animation-duration:12s;">
        💗
    </span>

    <span class="corazon"
          style="left:83%; font-size:23px; animation-duration:9s; animation-delay:4s;">
        ❤️
    </span>

    <span class="corazon"
          style="left:94%; font-size:30px; animation-duration:11s;">
        💕
    </span>

</div>



<!-- ==================================
     PORTADA
================================== -->

<div class="contenedor">

    <div class="titulo">

        <h1>
            Te amo plecioso
        </h1>

        <p>
            PARA EL AMOR DE MI VIDA
        </p>

    </div>


    <!-- SOBRE -->

    <div
        class="sobre"
        id="sobre"
        onclick="abrirSobre()"
    >

        <div class="cuerpo"></div>


        <div class="mini-carta">

            <h2>
                Para ti ❤️
            </h2>

            <p>
                Tengo algo que quiero decirte...
            </p>

        </div>


        <div class="tapa"></div>


        <div class="corazon-centro">
            ❤️
        </div>

    </div>


    <p class="instruccion">
        ❤️ Toca el sobre para abrir tu carta ❤️
    </p>

</div>



<!-- ==================================
     CARTA COMPLETA
================================== -->

<div
    class="carta-final"
    id="cartaFinal"
>


    <div class="papel">


        <div class="decoracion">
            ❤️ 💕 ❤️
        </div>


        <h2>
            Te amo plecioso
        </h2>


        <div class="texto">

            <p>
                <span class="amor">Mi amor,</span>
            </p>


            <p>
                Aprendí a programar para poder enviarte
                esta carta, y recordarte lo mucho que
                <span class="amor">
                    me encantas,
                </span>
                me fascinas, y te amo.
            </p>


            <p>
                Sí, amor...
                <span class="amor">
                    estoy muy enamorada de ti.
                </span>
            </p>


            <p>
                Me has hechizado en cuerpo y alma.
                ❤️
            </p>


            <p>
                Te amo, te amo, te amo...
                💕❤️💕
            </p>


            <p>
                Y si para decirte todo lo que siento
                tengo que aprender mil cosas nuevas,
                entonces aprenderé mil cosas por ti.
            </p>


            <p>
                Porque eres alguien demasiado especial
                para mí y quería que tuvieras algo que
                viniera directamente de mi corazón.
            </p>


        </div>


        <div class="firma">

            Por Siempre tuya<br>

            -K ❤️

        </div>


        <button
            class="boton"
            onclick="cerrarCarta()"
        >

            Cerrar carta 💕

        </button>


    </div>

</div>



<script>

/* ==================================
   ABRIR SOBRE
================================== */

function abrirSobre() {

    const sobre =
        document.getElementById("sobre");

    const carta =
        document.getElementById("cartaFinal");


    sobre.classList.add("abierto");


    /*
       Esperamos a que el sobre
       termine de abrirse.
    */

    setTimeout(() => {

        carta.classList.add("mostrar");

    }, 1000);

}


/* ==================================
   CERRAR CARTA
================================== */

function cerrarCarta() {

    const sobre =
        document.getElementById("sobre");

    const carta =
        document.getElementById("cartaFinal");


    carta.classList.remove("mostrar");


    setTimeout(() => {

        sobre.classList.remove("abierto");

    }, 500);

}

</script>


</body>
</html>
