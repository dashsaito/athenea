<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Athenea 💕</title>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #ffd6f5, #d8c8ff, #cce7ff);
            min-height: 100vh;
            overflow-x: hidden;
            color: #4b3f72;
        }

        h1, h2 {
            font-family: 'Pacifico', cursive;
        }

        #login {
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .card {
            background: rgba(255, 255, 255, .9);
            padding: 40px;
            border-radius: 25px;
            width: 350px;
            text-align: center;
            box-shadow: 0 0 25px rgba(0, 0, 0, .15);
        }

        .card h1 {
            color: #8b5cf6;
            margin-bottom: 15px;
        }

        input {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: none;
            border-radius: 15px;
            background: #f5eeff;
        }

        button {
            background: #b388ff;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 15px;
            cursor: pointer;
            transition: .3s;
            margin: 5px;
        }

        button:hover {
            transform: scale(1.05);
        }

        #contenido {
            display: none;
            padding-bottom: 50px;
        }

        .hero {
            text-align: center;
            padding: 50px 20px;
        }

        .hero h1 {
            font-size: 3rem;
            color: #7c3aed;
        }

        .foto-athenea {
            text-align: center;
            margin-top: 20px;
        }

        .foto-athenea img {
            width: 250px;
            height: 250px;
            object-fit: cover;
            border-radius: 50%;
            border: 6px solid white;
            box-shadow: 0 0 30px rgba(179, 136, 255, .8);
        }

        .latido {
            font-size: 50px;
            animation: latir 1s infinite;
        }

        @keyframes latir {
            50% { transform: scale(1.2); }
        }

        .contador {
            text-align: center;
            font-size: 1.5rem;
            font-weight: bold;
            color: #7c3aed;
            margin: 30px;
        }

        .galeria {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            padding: 20px;
        }

        .galeria img {
            width: 280px;
            border-radius: 20px;
            box-shadow: 0 0 15px rgba(0, 0, 0, .15);
        }

        .carta, .lista, #mensajeCarta, .razones {
            max-width: 900px;
            margin: 30px auto;
            background: white;
            padding: 30px;
            border-radius: 25px;
            box-shadow: 0 0 15px rgba(0, 0, 0, .1);
            line-height: 1.8;
        }

        .cartas {
            text-align: center;
            margin-top: 40px;
        }

        .cancion {
            background: #f8f1ff;
            padding: 15px;
            margin-top: 15px;
            border-radius: 15px;
        }

        .amor {
            text-align: center;
            margin-top: 50px;
            position: relative;
            height: 250px;
        }

        #no {
            position: absolute;
            left: 55%;
            top: 80px;
            transition: all 0.2s ease;
        }

        #respuesta {
            margin-top: 60px;
            font-size: 1.5rem;
            font-weight: bold;
            color: #7c3aed;
        }

        .final {
            text-align: center;
            margin-top: 60px;
        }

        .boton-sorpresa {
            display: block;
            margin: 40px auto;
            font-size: 20px;
            padding: 15px 30px;
            background: linear-gradient(45deg, #ffb6e6, #c9a0ff);
            border: none;
            border-radius: 25px;
            color: white;
            font-family: 'Pacifico', cursive;
            box-shadow: 0 0 15px rgba(179, 136, 255, .5);
        }

        .foto-final {
            margin-top: 20px;
        }

        .foto-final img {
            width: 300px;
            max-width: 90%;
            border-radius: 20px;
            border: 5px solid white;
            box-shadow: 0 0 20px rgba(179, 136, 255, .6);
        }

        #pagina2 {
            display: none;
            padding: 40px;
            text-align: center;
            min-height: 100vh;
            background: linear-gradient(135deg, #ffe0f5, #e2d1ff, #dff1ff);
        }

        #pagina2 h1 {
            font-size: 3rem;
            color: #7c3aed;
            margin-bottom: 20px;
        }

        .volver {
            margin-top: 30px;
            font-family: 'Pacifico', cursive;
        }

        .corazon, .sakura {
            position: fixed;
            top: -20px;
            font-size: 25px;
            z-index: 999;
            pointer-events: none;
        }

        .corazon { animation: caer linear forwards; }
        .sakura { animation: caerSakura linear forwards; }

        @keyframes caer {
            to {
                transform: translateY(110vh);
                opacity: 0;
            }
        }

        @keyframes caerSakura {
            to {
                transform: translateY(110vh) rotate(360deg);
                opacity: 0;
            }
        }
    </style>
</head>

<body>

    <div id="login">
        <div class="card">
            <h1>Bienvenida, mi amor</h1>
            <p>Ingresa el nombre del amor de vida de Dash</p>
            <input type="text" id="nombre" placeholder="Nombre">
            <p>Ingresa lo que siempre te digo</p>
            <input type="password" id="password" placeholder="Contraseña">
            <button onclick="entrar()">Entrar</button>
            <p id="error" style="color:red; margin-top: 10px;"></p>
        </div>
    </div>

    <div id="contenido">
        <div class="hero">
            <h1>Athenea</h1>
            <div class="latido">ᡣ𐭩</div>
            <p>Gracias por estos hermosos 5 meses juntos.</p>
        </div>

        <div class="foto-athenea">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYRJ5xvCZKVxFLQJW_M1ZPqdiUCS4dkTUHzkvTYFDeSdlTW1r1Va1mLNs&s=10" alt="Athenea">
        </div>

        <div id="dias" class="contador"></div>

        <div class="galeria">
            <img src="https://media.vandalsports.com/i/640x360/12-2025/2025123163510_1.jpg" alt="Galeria">
        </div>

        <div class="carta">
            <h2>💌 Para Athenea 💌</h2>
            <p>Gracias por estos meses tan especiales.</p>
            <p>Naciste el 11 de octubre de 2008 y desde que llegaste a mi vida lograste hacer mis días más felices.</p>
            <p>Me gustan tus ojos, tu sonrisa, tu cabello y la forma tan especial en que me haces sentir.</p>
            <p>Aunque estemos lejos, cada mensaje y momento contigo vale muchísimo para mí.</p>
            <p>Me encanta escuchar hablar de las cosas que te gustan, especialmente de Gachiakuta, o escucharte hablar de todo, incluso de lo mínimo.</p>
            <p>Nunca olvidaré cómo nos conocimos en aquel team de rol donde tú eras Dabi y yo Sero Hanta.</p>
            <p>Gracias por acompañarme durante estos meses.</p>
            <p>Te amo de aquí a la luna a pasitos de tortuga <3</p>
        </div>

        <div class="lista">
            <h2>Nuestras Coincidencias ¿? ✨</h2>
            <ul>
                <li>Nos conocimos en un team de rol.</li>
                <li>Tú siendo Dabi.</li>
                <li>Yo siendo Sero.</li>
                <li>Compartimos nuestro gusto por el anime.</li>
                <li>La distancia nunca nos detuvo.</li>
                <li>Cada día seguimos construyendo algo bonito.</li>
            </ul>
        </div>

        <div class="carta">
            <h2>Nuestras Canciones 🎵</h2>
            <p>Esta sección está dedicada a las canciones que me recuerdan a ti.</p>
            
            <div class="cancion">
                <h3>M.</h3>
                <p>
                    Era obvio desde la primera noche... ¿Dónde estabas entonces?<br>
                    Como te besaba en esos momentos, no puedes decir basta a esto.<br>
                    Tus palabras, tus ojos, tus manos solo para mí.<br>
                    Mis esperanzas, mi sonrisa, mi sueño solo para ti.<br><br>
                    Cuando no puedo encontrarte, me pierdo.<br>
                    Ahora, en el cielo, yo con tus manos me encuentro bailando.<br><br>
                    Llévame contigo, cariño. Devuélveme a ti, cariño.<br>
                    Por favor vuelve, cariño. Devuélveme a ti, cariño.
                </p>
            </div>

            <div class="cancion">
                <h3>Mi kryptonita - Doble ONE Flow Letal</h3>
                <p>
                    Quiere que le ruegue y, cómo no, si está preciosa...<br>
                    Por eso me domina, para un loco hay una loca.<br>
                    Me gusta ese vestido que te pones color rosa.<br>
                    ¿Por qué no me callas a besos de una vez la boca?<br>
                    Me encanta su anatomía, verla me provoca...
                </p>
            </div>
        </div>

        <div class="cartas">
            <h2>💌 Cartas Secretas 💌</h2>
            <button onclick="abrirCarta(1)">Carta 1</button>
            <button onclick="abrirCarta(2)">Carta 2</button>
            <button onclick="abrirCarta(3)">Carta 3</button>
            <div id="mensajeCarta">Haz clic en una carta ♡</div>
        </div>

        <div class="amor">
            <h2>¿Me amas?</h2>
            <button onclick="si()">Sí</button>
            <button id="no" onmouseover="escapar()">No 💔</button>
            <p id="respuesta"></p>
        </div>

        <div class="final">
            <button onclick="abrirPagina2()" class="boton-sorpresa">💜 100 Razones Para Amarte 💜</button>
            <h1>Feliz 5 Meses Juntos️ 💕</h1>
            <p>Gracias por cada momento compartido.</p>
            <p>Con cariño, Dash 🫪</p>
            <div class="foto-final">
                <img src="https://i.pinimg.com/236x/b6/f6/82/b6f682e4eba14b81513387f58f227e5f.jpg" alt="Amor">
                <p>Mi lugar favorito siempre será contigo y en donde tú estés 𖹭.</p>
            </div>
        </div>
    </div>

    <div id="pagina2">
        <h1>100 Razones Para Amarte</h1>
        <div class="razones">
            <p>
                1. Porque me haces sentir en paz.<br><br>
                2. Porque me gusta hablar contigo.<br><br>
                3. Porque escuchas mis problemas.<br><br>
                4. Porque confías en mí.<br><br>
                5. Porque me haces sonreír.<br><br>
                6. Porque me haces sentir importante.<br><br>
                7. Porque me apoyas.<br><br>
                8. Porque me haces sentir querido.<br><br>
                9. Porque me entiendes.<br><br>
                10. Porque eres auténtica.<br><br>
                11. Porque eres especial para mí.<br><br>
                12. Porque siempre pienso en ti.<br><br>
                13. Porque me gusta tu forma de ver las cosas.<br><br>
                14. Porque me haces sentir acompañado.<br><br>
                15. Porque me inspiras a seguir adelante.<br><br>
                16. Porque me gusta pasar tiempo contigo.<br><br>
                17. Porque me gusta escuchar tu voz.<br><br>
                18. Porque me haces sentir afortunado.<br><br>
                19. Porque me das confianza.<br><br>
                20. Porque eres una persona dulce.<br><br>
                21. Porque eres fuerte.<br><br>
                22. Porque eres valiente.<br><br>
                23. Porque eres inteligente.<br><br>
                24. Porque eres divertida.<br><br>
                25. Porque me haces reír incluso en días malos.<br><br>
                26. Porque contigo puedo ser yo mismo.<br><br>
                27. Porque me aceptas.<br><br>
                28. Porque me haces sentir tranquilo.<br><br>
                29. Porque me gusta cómo me tratas.<br><br>
                30. Porque siempre encuentro algo nuevo que admirar de ti.<br><br>
                31. Porque me haces ilusión cada día.<br><br>
                32. Porque me encanta recibir tus mensajes.<br><br>
                33. Porque me alegras la mañana.<br><br>
                34. Porque me alegras la noche.<br><br>
                35. Porque haces especiales los días normales.<br><br>
                36. Porque me gusta tu forma de pensar.<br><br>
                37. Porque eres cariñosa.<br><br>
                38. Porque eres amable.<br><br>
                39. Porque eres paciente conmigo.<br><br>
                40. Porque me haces sentir comprendido.<br><br>
                41. Porque me gusta compartir mis sueños contigo.<br><br>
                42. Porque me gusta escuchar tus sueños.<br><br>
                43. Porque me haces sentir seguro.<br><br>
                44. Porque me gusta tu manera de expresarte.<br><br>
                45. Porque me gusta cuando te emocionas por algo.<br><br>
                46. Porque me gusta aprender cosas de ti.<br><br>
                47. Porque haces que la distancia parezca menos grande.<br><br>
                48. Porque me haces sentir cerca incluso estando lejos.<br><br>
                49. Porque me gusta recordar cómo nos conocimos.<br><br>
                50. Porque me gusta imaginar el futuro contigo.<br><br>
                51. Porque me haces creer más en mí.<br><br>
                52. Porque me motivas.<br><br>
                53. Porque eres parte importante de mis días.<br><br>
                54. Porque me gusta cuando me cuentas cosas de tu día.<br><br>
                55. Porque me gusta cuando compartimos nuestras emociones.<br><br>
                56. Porque haces que todo valga la pena.<br><br>
                57. Porque me haces sentir feliz.<br><br>
                58. Porque eres una persona única.<br><br>
                59. Porque me haces sentir afortunado de haberte conocido.<br><br>
                60. Porque me gusta cómo cuidas a las personas que quieres.<br><br>
                61. Porque tienes un corazón bonito.<br><br>
                62. Porque eres sincera.<br><br>
                63. Porque eres especial.<br><br>
                64. Porque me haces sentir escuchado.<br><br>
                65. Porque me gusta tu compañía.<br><br>
                66. Porque me gusta tu energía.<br><br>
                67. Porque me haces sentir valorado.<br><br>
                68. Porque me gusta compartir mis logros contigo.<br><br>
                69. Porque me gusta celebrar tus logros.<br><br>
                70. Porque me haces sentir menos solo.<br><br>
                71. Porque me haces sentir querido por quien soy.<br><br>
                72. Porque me gusta cuando te ríes.<br><br>
                73. Porque me gusta cuando eres feliz.<br><br>
                74. Porque me importa tu bienestar.<br><br>
                75. Porque me gusta cuidarte.<br><br>
                76. Porque me gusta saber de ti.<br><br>
                77. Porque me gusta verte emocionada.<br><br>
                78. Porque me haces sentir especial.<br><br>
                79. Porque haces mis días mejores.<br><br>
                80. Porque eres una parte importante de mi vida.<br><br>
                81. Porque me haces sentir comprendido.<br><br>
                82. Porque me gusta pensar en ti.<br><br>
                83. Porque me gusta imaginar momentos contigo.<br><br>
                84. Porque me gusta compartir recuerdos contigo.<br><br>
                85. Porque me haces sentir tranquilidad.<br><br>
                86. Porque me gusta tu personalidad.<br><br>
                87. Porque eres increíble.<br><br>
                88. Porque eres tierna.<br><br>
                89. Porque eres una buena persona.<br><br>
                90. Porque me haces sonreír sin darme cuenta.<br><br>
                91. Porque me gusta hablar contigo durante horas.<br><br>
                92. Porque siempre encuentro razones para quererte más.<br><br>
                93. Porque haces que los días difíciles sean más fáciles.<br><br>
                94. Porque me haces sentir afortunado.<br><br>
                95. Porque eres importante para mí.<br><br>
                96. Porque me gusta cómo eres.<br><br>
                97. Porque me gusta estar contigo.<br><br>
                98. Porque me haces feliz.<br><br>
                99. Porque me haces sentir amado.<br><br>
                100. Porque cada día encuentro una razón nueva para quererte más.<br><br>
                Y por muchas razones podrían resumirse en una sola: <strong>porque eres Athenea. 💜</strong>
            </p>
            <img src="https://i.pinimg.com/736x/55/5d/e2/555de2bdbcb4f8a1d8ef9d4427bbd4c6.jpg" style="width:300px;border-radius:20px;margin-top:20px;" alt="Love">
            <br>
            <button class="volver" onclick="volverPagina1()">🌸 Volver 🌸</button>
        </div>
    </div>

    <script>
        function entrar() {
            let nombre = document.getElementById("nombre").value.trim().toLowerCase();
            let pass = document.getElementById("password").value.trim().toLowerCase();

            if (nombre === "athenea" && pass === "teamo") {
                document.getElementById("login").style.display = "none";
                document.getElementById("contenido").style.display = "block";

                actualizarContador();
                crearCorazones();
                crearSakura();
            } else {
                document.getElementById("error").innerHTML = "Nombre o contraseña incorrectos 💔";
            }
        }

        function actualizarContador() {
            // Tu contador original intacto
            const inicio = new Date("2026-02-13");
            const hoy = new Date();

            const dias = Math.floor(
                (hoy - inicio) / (1000 * 60 * 60 * 24)
            );

            document.getElementById("dias").innerHTML = `💞 Llevamos ${dias} días juntos 💞`;
        }

        function abrirCarta(numero) {
            let texto = "";
            if (numero === 1) {
                texto = "Gracias por cada mensaje que ilumina mis días. Levantarme y verte en mi foto de pantalla me llena de vida, me das fuerzas para seguir luchando, seguir siendo fuerte y aguantar el estrés. Te amo.";
            }
            if (numero === 2) {
                texto = "Aunque haya kilómetros entre nosotros, siempre te siento cerca. Nunca dudes de lo mucho que te amo. A cada segundo, a cada minuto, mi mente y cuerpo son tuyos. Me gustas, me encantas de la manera más hermosa, porque te amo y te respeto. Me fascina todo de ti, quiero que cada mirada, cada respiro, cada risa, sea mía de la manera mas enferma y obseciva posible y egoista Te quiero para mí para construir un futuro juntos para casarnos y qur seas la madre de mis hijos.";
            }
            if (numero === 3) {
                texto = "Eres una de las personas más importantes para mí. Me encanta cómo me tratas, me haces sentir el hombre más amado del mundo y quisiera poder hacerte sentir así a ti siempre. Te amo.";
            }
            document.getElementById("mensajeCarta").innerHTML = texto;
        }

        function si() {
            document.getElementById("respuesta").innerHTML = "¡Yo también te amo muchísimo, Athenea! 💖✨";
        }

        function escapar() {
            let boton = document.getElementById("no");
            let x = Math.random() * 70; // Porcentaje horizontal
            let y = Math.random() * 150 + 50; // Pixeles verticales

            boton.style.left = x + "%";
            boton.style.top = y + "px";
        }

        function crearCorazones() {
            setInterval(() => {
                let corazon = document.createElement("div");
                corazon.innerHTML = "🦭"; 
                corazon.classList.add("corazon");
                corazon.style.left = Math.random() * 100 + "vw";
                corazon.style.animationDuration = (Math.random() * 3 + 2) + "s";
                document.body.appendChild(corazon);

                setTimeout(() => { corazon.remove(); }, 4000);
            }, 400);
        }

        function crearSakura() {
            setInterval(() => {
                let flor = document.createElement("div");
                flor.innerHTML = "🌸";
                flor.classList.add("sakura");
                flor.style.left = Math.random() * 100 + "vw";
                flor.style.animationDuration = (Math.random() * 5 + 4) + "s";
                document.body.appendChild(flor);

                setTimeout(() => { flor.remove(); }, 8000);
            }, 500);
        }

        function abrirPagina2() {
            document.getElementById("contenido").style.display = "none";
            document.getElementById("pagina2").style.display = "block";
            window.scrollTo(0, 0);
        }

        function volverPagina1() {
            document.getElementById("pagina2").style.display = "none";
            document.getElementById("contenido").style.display = "block";
            window.scrollTo(0, 0);
        }
    </script>
</body>
</html>
