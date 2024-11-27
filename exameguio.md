

```markdown
# HTML con Divisiones

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML con Divisiones</title>
    <link rel="stylesheet" href="estilos.css"> <!-- Puedes enlazar tu archivo CSS aquí -->
    <script src="script.js"></script>
</head>
<body>

<!-- Si es id: -->
#header {
  background-color: #3498db;
  color: white;
}

<!-- Si es class: -->
.box {
  background-color: #2c3e50;
  color: white;
  padding: 20px;
}

<!-- Si es div: -->
div {
  background-color: #ecf0f1;
  padding: 10px;
}

<!-- Si es id con class: -->
#contenedor .box {
  background-color: #2c3e50;
  color: white;
  padding: 20px;
}

a:hover {
  color: red;
}

a:hover {
  cursor: pointer; /* Cambia el cursor a una mano, indicando que es un enlace */
}

div:hover {
  transform: scale(1.1); /* Aumenta el tamaño del elemento */
  transition: transform 0.3s ease; /* Transición suave */
}

</body>
</html>
```

## JS para cambiar el color

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo Hover JS</title>
    <style>
        a {
            text-decoration: none;
            color: blue;
        }
    </style>
</head>
<body>

<a href="https://www.example.com" id="enlace">Visitar página</a>

<script>
    // Selecciona el enlace por su ID
    const enlace = document.getElementById('enlace');

    // Añadir evento mouseover para cambiar el color
    enlace.addEventListener('mouseover', function() {
        enlace.style.color = 'red';  // Cambia el color del texto a rojo
    });

    // Añadir evento mouseout para restaurar el color original
    enlace.addEventListener('mouseout', function() {
        enlace.style.color = 'blue';  // Restaura el color original
    });
</script>

</body>
</html>
```

## Cambio de color con transición

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Transición con JavaScript</title>
    <style>
        #miCaja {
            width: 200px;
            height: 200px;
            background-color: #3498db;
            transition: background-color 0.5s ease; /* Transición suave de color */
        }
    </style>
</head>
<body>

<div id="miCaja"></div>

<script>
    // Selecciona el div
    const miCaja = document.getElementById('miCaja');

    // Cambiar el color de fondo cuando el ratón pasa sobre el div
    miCaja.addEventListener('mouseover', function() {
        miCaja.style.backgroundColor = '#2ecc71'; // Cambia el color a verde
    });

    // Restaurar el color original cuando el ratón sale
    miCaja.addEventListener('mouseout', function() {
        miCaja.style.backgroundColor = '#3498db'; // Restaura el color original (azul)
    });
</script>

</body>
</html>
```

## Ejemplos de Topbar

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Top Bar Ejemplo</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Barra superior -->
    <header id="topBar">
        <div class="container">
            <h1>Mi Web</h1>
            <nav>
                <ul id="menuList">
                    <li><a href="#home">Inicio</a></li>
                    <li><a href="#about">Sobre nosotros</a></li>
                    <li><a href="#services">Servicios</a></li>
                    <li><a href="#contact">Contacto</a></li>
                </ul>
                <div id="hamburgerIcon">&#9776;</div>
            </nav>
        </div>
    </header>

    <!-- Contenido -->
    <section id="content">
        <div class="section" id="home">Bienvenido a la página principal.</div>
        <div class="section" id="about">Sobre nosotros.</div>
        <div class="section" id="services">Servicios.</div>
        <div class="section" id="contact">Contacto.</div>
    </section>

    <script src="scripts.js"></script>

</body>
</html>
```

## CSS para Topbar

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
}

#topBar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #3498db;
  padding: 10px 0;
  color: white;
  text-align: center;
  z-index: 1000;
}

#topBar nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
}

#topBar nav ul li {
  margin: 0 15px;
}

#topBar nav ul li a {
  text-decoration: none;
  color: white;
  font-weight: bold;
}

#topBar nav ul li a:hover {
  color: #f39c12;
}

#hamburgerIcon {
  display: none;
  font-size: 30px;
  cursor: pointer;
}

#content {
  margin-top: 80px;
  padding: 20px;
}

.section {
  padding: 50px;
  background-color: #f4f4f4;
  margin: 20px 0;
}

@media (max-width: 768px) {
  #topBar nav ul {
    display: none;
    flex-direction: column;
  }

  #topBar nav.active ul {
      display: flex;
  }

  #hamburgerIcon {
    display: block;
  }
}
```

## JavaScript para Topbar

```javascript
window.onscroll = function() {
  const topBar = document.getElementById('topBar');
  if (window.scrollY > 50) {
    topBar.style.backgroundColor = '#2c3e50'; // Cambiar color de la barra
  } else {
    topBar.style.backgroundColor = '#3498db'; // Color original
  }
};

// Mostrar/ocultar el menú al hacer clic en el icono de hamburguesa
const hamburgerIcon = document.getElementById('hamburgerIcon');
const menuList = document.getElementById('menuList');

hamburgerIcon.onclick = function() {
  menuList.classList.toggle('active');
};
```

## Botón cambia color

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cambiar Color</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Elemento cuyo color cambia -->
    <div id="miElemento" class="caja">
        Este es el elemento cuyo color cambiará.
    </div>

    <!-- Botón que activará el cambio de color -->
    <button id="botonCambiarColor">Cambiar Color</button>

    <!-- Vinculamos el archivo JS -->
    <script src="scripts.js"></script>

</body>
</html>
```

## CSS para Botón Cambia Color

```css
.caja {
  width: 200px;
  height: 200px;
  background-color: lightblue; /* Color inicial */
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px auto;
  border-radius: 10px;
  font-size: 18px;
  color: white;
}

button {
  display: block;
  margin: 20px auto;
  padding: 10px 20px;
  background-color: #3498db;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #2980b9;
}
```

## JavaScript para Botón Cambia Color

```javascript
const boton = document.getElementById('botonCambiarColor');
const elemento = document.getElementById('miElemento');

// Función para cambiar el color
boton.addEventListener('click', function() {
  // Cambiar el color de fondo del elemento
  elemento.style.backgroundColor = 'lightgreen';
});
```

Este es el código convertido a **Markdown**. Puedes copiar y pegar este contenido directamente en cualquier archivo Markdown para tener una buena referencia de los ejemplos que has solicitado.
