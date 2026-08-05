<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ultimo Trabajo de Electiva Desarrollo Web 1</title>
    

    <style>
        /* --- RESET Y ESTILOS GENERALES --- */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, BlinkMacSystemFont, 'Roboto', 'Helvetica Neue', sans-serif;
            -webkit-font-smoothing: antialiased;
            color: #333;
            background-color: #e5e6ed;
        }

        html {
            scroll-behavior: smooth;
        }

    

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- NAVBAR ESTILIZADO --- */
        .header {
            background-color: #ffffff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 60px;
        }

        .brand-logo {
            font-size: 1.3rem;
            font-weight: 700;
            color: #2c3e50;
            text-decoration: none;
        }

        .brand-logo span {
            color: #0d6efd;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 20px;
            
        }

        .nav-link {
            text-decoration: none;
            color: #495057;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.3s ease;
        }

        .nav-link:hover, .nav-link.active {
            color: #0d6efd;
        }

        /* --- CONTENIDO PRINCIPAL --- */
        .main-content {
            padding: 40px 0;
        }

        #titlep {
            font-weight: 300;
            letter-spacing: -0.5px;
            color: #2c3e50;
            margin-bottom: 20px;
            font-size: 2rem;
        }

        /* --- TARJETA DEL PÁRRAFO CON SOMBRA MÁS PRONUNCIADA --- */
        .tarjeta-parrafo {
            border: 1px dashed #b6d4fe;
            padding: 25px;
            border-radius: 12px;
            margin-bottom: 35px;
            background-color: #ffffff;
            /* SOMBRA MÁS INTENSA Y DEFINIDA */
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.22);
            transition: box-shadow 0.3s ease, transform 0.3s ease;
        }

        .tarjeta-parrafo:hover {
            box-shadow: 0 14px 30px rgba(0, 0, 0, 0.30);
            transform: translateY(-2px);
            transition: box-shadow 0.3s ease, transform 0.3s ease;
        }

        .tarjeta-parrafo p {
            line-height: 1.7;
            color: #495057;
            font-size: 0.95rem;
            font-weight: 300;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.22);
        }

        .tarjeta-parrafo p strong {
            font-weight: 600;
            color: #212529;
            
        }

        /* --- SECCIONES Y VISORES --- */
        #lenguajes h1, #frameworks h1, #os h1 {
            font-size: 1.35rem;
            font-weight: 400;
            letter-spacing: 0.2px;
            margin-bottom: 14px;
            color: #2b2b2b;
        }

        #visorlenguajes, 
        #visorframeworks, 
        #visorsoperativos {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            border: 1.5px solid #cfe2ff;
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 40px;
            background-color: #ffffff;
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.05);
        }

        #visorlenguajes > div, 
        #visorframeworks > div, 
        #visorsoperativos > div {
            border: 1px solid #e7f1ff;
            padding: 22px 16px;
            text-align: center;
            border-radius: 10px;
            background-color: #ffffff;
            display: flex;
            flex-direction: column;
            align-items: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            transition: transform 0.25s ease, box-shadow 0.25s ease;
            max-width: 320px;
            height: auto;
        }

        #visorlenguajes > div:hover, 
        #visorframeworks > div:hover, 
        #visorsoperativos > div:hover {
            transform: translateY(-4px);
            box-shadow: 0 10px 30px rgba(45, 13, 253, 0.18);
            transition: transform 0.25s ease, box-shadow 0.25s ease;
        }

        #visorlenguajes div img, 
        #visorframeworks div img, 
        #visorsoperativos div img {
            width: 90px;
            height: 90px;
            border-radius: 50%;
            border: 1.5px solid #0c4698;
            object-fit: cover;
            object-position: center;
            margin-bottom: 20px;
            display: block;
            background-color: #f8f9fa;
            box-shadow: 0 100px 250px rgba(0, 0, 0, 0.22);
            transform: translateY(-4px);
            transition: transform 0.25s ease, box-shadow 0.25s ease;
        }

        #visorlenguajes h4, 
        #visorframeworks h4, 
        #visorsoperativos h4 {
            margin: 0 0 8px 0;
            font-size: 1.05rem;
            font-weight: 500;
            color: #2c3e50;
            box-shadow: 0 100px 250px rgba(0, 0, 0, 0.22);
        }

        #visorlenguajes p, 
        #visorframeworks p, 
        #visorsoperativos p {
            font-size: 0.85rem;
            color: #6c757d;
            line-height: 1.5;
            font-weight: 300;
            box-shadow: 0 100px 250px rgba(0, 0, 0, 0.22);
        }

        /* --- FOOTER --- */
        .footer {
            background-color: #2c3e50;
            color: #ffffff;
            padding: 30px 0 15px;
            margin-top: 40px;
            box-shadow: 0 10px 21px rgba(0, 0, 0, 0.22);
            border-radius: 5%;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-bottom: 20px;
            box-shadow: 0 10px 21px rgba(0, 0, 0, 0.22);
            border-radius: 5%;
            
        }

        .footer-col h4 {
            margin-bottom: 10px;
            color: #cfe2ff;
        }

        .footer-col p, .footer-col ul {
            font-size: 0.85rem;
            color: #0e7cc5;
            line-height: 1.6;
            
        }

        .footer-col ul {
            list-style: none;
            
        }

        .footer-col a {
            color: #bdc3c7;
            text-decoration: none;
        }

        .footer-bottom {
            text-align: center;
            font-size: 0.8rem;
            color: #08e15b;
            border-top: 1px solid #34495e;
            padding-top: 15px;
        }

        /* Responsive */
        @media (max-width: 750px) {
            #visorlenguajes, #visorframeworks, #visorsoperativos {
                grid-template-columns: repeat(2, 1fr);
                box-shadow: 0 10px 250px rgba(0, 0, 0, 0.22);
            }
            .footer-grid {
                grid-template-columns: 1fr;
                box-shadow: 0 10px 250px rgba(0, 0, 0, 0.22);
            }
        }
        @media (max-width: 480px) {
            #visorlenguajes, #visorframeworks, #visorsoperativos {
                grid-template-columns: 1fr;
                box-shadow: 0 10px 250px rgba(0, 0, 0, 0.22);
            }
        }
        
    </style>
</head>

<body>

    <!-- NAVBAR -->
    <header class="header">
        <div class="container navbar">
            <a href="#" class="brand-logo">Mi<span>Sitio Web interactivo</span></a>
            <nav>
                <ul class="nav-menu" id="nav-menu">
                    <li class="nav-item"><a href="#frameworks" class="nav-link">Lenguajes</a></li>
                    <li class="nav-item"><a href="#frameworks" class="nav-link">Frameworks</a></li>
                    <li class="nav-item"><a href="#os" class="nav-link">S.Operativos</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- CONTENIDO PRINCIPAL -->
    <main class="main-content">
        <div class="container">
            <h1 id="titlep" box-shadow: 0 100px 25px rgba(0, 0, 0, 0.22);>Bienvenidos al Ultimo Examen de Electiva Web 1</h1>

            <!-- TARJETA DE INTRODUCCIÓN CON LA CLASE CON MÁS SOMBRA -->

            <div id="intro" class="tarjeta-parrafo">
                <p>
                    <br>Programar es el arte de transformar ideas abstractas en instrucciones l&oacute;gicas que las
                    computadoras puedan ejecutar. A trav&eacute;s de <strong>lenguajes de
                    programaci&oacute;n</strong> como Python, C# o JavaScript, construimos la arquitectura
                    b&aacute;sica de cualquier software. Para agilizar este proceso existen los
                    <strong>frameworks</strong> —como React, Django o Flutter—, estructuras predefinidas que evitan
                    "reinventar la rueda", offrant herramientas listas para usar que mejoran la seguridad, la
                    mantenibilidad y la velocidad de desarrollo. Todo este ecosistema cobra vida sobre los
                    <strong>sistemas operativos</strong>: <strong>Linux</strong> lidera en servidores y desarrollo
                    backend; <strong>Windows</strong> domina el sector empresarial y de videojuegos;
                    <strong>macOS</strong> es la plataforma clave para el ecosistema Apple; mientras que
                    <strong>Android e iOS</strong> reciben aplicaciones m&oacute;viles nativas o construidas
                    mediante frameworks multiplataforma. En conjunto, el lenguaje aporta la l&oacute;gica, el
                    framework acelera la creaci&oacute;n y el sistema operativo proporciona el terreno donde la
                    tecnolog&iacute;a finalmente se ejecuta.</br>

                    <br>El <strong>Código:</strong> Son las líneas de texto e instrucciones que escribe la persona programadora.</br>
                    <br>El <strong>Lenguaje:</strong> Se usan idiomas especiales (como Python o Java) para que la computadora entienda las órdenes.</br>
                    <br>La <strong>Ejecucion:</strong> La máquina lee el código y hace exactamente lo que se le pide sin dudar.</br>
                </p>
            </div>

            <!-- SECCIÓN LENGUAJES -->
            <div id="lenguajes">
                <h1>Lenguajes</h1>
            </div>
            <div id="visorlenguajes">
                <div>
                    <img src="csharp.jpg" alt="C Sharp">
                    <h4>C Sharp</h4>
                    <p>Lenguaje multiparadigma desarrollado por Microsoft para la plataforma .NET.</p>
                </div>
                <div>
                    <img src="java.jpg" alt="Java">
                    <h4>Java</h4>
                    <p>Lenguaje orientado a objetos enfocado en la portabilidad entre plataformas.</p>
                </div>
                <div>
                    <img src="js.jpg" alt="JavaScript">
                    <h4>JavaScript</h4>
                    <p>Lenguaje clave para el desarrollo web interactivo en el cliente y servidor.</p>
                </div>
                <div>
                    <img src="php.jpg" alt="PHP">
                    <h4>PHP</h4>
                    <p>Lenguaje de programación del lado del servidor ampliamente usado en la web.</p>
                </div>
                <div>
                    <img src="python.jpg" alt="Python">
                    <h4>Python</h4>
                    <p>Lenguaje versátil y de sintaxis limpia usado en IA, web y ciencia de datos.</p>
                </div>
            </div>

            <!-- SECCIÓN FRAMEWORKS -->
            <div id="frameworks">
                <h1>Frameworks</h1>
            </div>
            <div id="visorframeworks">
                <div>
                    <img src="angular.jpg" alt="Angular">
                    <h4>Angular</h4>
                    <p>Framework de desarrollo web creado por Google para aplicaciones SPA.</p>
                </div>
                <div>
                    <img src="django.jpg" alt="Django">
                    <h4>Django</h4>
                    <p>Framework web de alto nivel basado en Python enfocado en rapidez y diseño limpio.</p>
                </div>
                <div>
                    <img src="laravel.jpg" alt="Laravel">
                    <h4>Laravel</h4>
                    <p>Framework de desarrollo web en PHP con sintaxis elegante y expresiva.</p>
                </div>
                <div>
                    <img src="svelty.jpg" alt="Svelte">
                    <h4>Svelte</h4>
                    <p>Compilador que convierte componentes en código JavaScript eficiente sin Virtual DOM.</p>
                </div>
                <div>
                    <img src="vue.jpg" alt="Vue.js">
                    <h4>Vue.js</h4>
                    <p>Framework progresivo de JavaScript para la construcción de interfaces de usuario.</p>
                </div>
            </div>

            <!-- SECCIÓN SISTEMAS OPERATIVOS -->
            <div id="os">
                <h1>Sistemas Operativos</h1>
            </div>
            <div id="visorsoperativos">
                <div>
                    <img src="android.jpg" alt="Android">
                    <h4>Android</h4>
                    <p>Sistema operativo móvil desarrollado por Google basado en el núcleo Linux.</p>
                </div>
                <div>
                    <img src="ios.jpg" alt="iOS">
                    <h4>iOS</h4>
                    <p>Sistema operativo móvil de Apple exclusivo para sus dispositivos iPhone.</p>
                </div>
                <div>
                    <img src="linux.jpg" alt="Linux">
                    <h4>Linux</h4>
                    <p>Sistema operativo de código abierto ampliamente utilizado en servidores y desarrollo.</p>
                </div>
                <div>
                    <img src="macos.jpg" alt="macOS">
                    <h4>macOS</h4>
                    <p>Sistema operativo de escritorio desarrollado por Apple para sus computadoras Mac.</p>
                </div>
                <div>
                    <img src="windows.jpg" alt="Windows" >
                    <h4>Windows</h4>
                    <p>Sistema operativo dominante en el entorno empresarial y de videojuegos.</p>
                </div>
            </div>
        </div>
    </main>

    <!-- FOOTER -->
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <h4>Mi Sitio Web</h4>
                    <p>Una plantilla base moderna y lista para tus proyectos.</p>
                </div>
                <div class="footer-col">
                    <h4>Navegación</h4>
                    <ul>
                        <li><a href="#">Inicio</a></li>
                        <li><a href="#lenguajes">Lenguajes</a></li>
                        <li><a href="#frameworks">Frameworks</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Contacto</h4>
                    <p>Email: info@misitio.com</p>
                </div>
            </div>

            <div class="footer-bottom">
                <p>&copy; 2026 MiSitio Web. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

</body>

</html>
