# laboratorio-1
El laboratorio uno se trata sobre un calculador que determina tu edad. Aqui detallo los archivos necesarios para hacer que funcione.

index.html
Es el código que se utiliza para estructurar y desplegar una página web y sus contenidos. Por ejemplo, sus contenidos podrían ser párrafos, 
una lista con viñetas, o imágenes y tablas de datos.

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="estilos.css">
    <title>Laboratorio #1</title>
</head>
<body>
    <h1>Calculador</h1>
<div id="contenedor">
    <input type="text" id="entrada" placeholder="Ingrese su edad aquí">
    <button id="agregar">Agregar</button>
    <h2 id="respuesta"></h2>
</div>
<ul id="lista">
</ul>
 <script src="app.js"></script>
</body>
</html>

estilos.css
Las CSS (hojas de estilo en cascada) son archivos codificados que seleccionan elementos de tu página y controlan su presentación. Piensa 
en el HTMLde tu plantilla personalizada como los huesos del sitio web y la CSS como la piel.

body{
    background-color: #fc3459;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;

}
h1{
    text-align: center;
    color: rgb(255, 255, 255);
}
#contenedor{
    text-align: center;
}
input{
    padding: 10px;
    font-size: 16px;
}
button{
    padding: 10px;
    cursor: pointer;
}

app.js
JavaScript es un lenguaje de programación que los desarrolladores utilizan para hacer páginas web interactivas. Desde actualizar fuentes
de redes sociales a mostrar animaciones y mapas interactivos, las funciones de JavaScript pueden mejorar la experiencia del usuario de un
sitio web.

const edad = document.getElementById("entrada");
const boton= document.getElementById("agregar");
const respuesta = document.getElementById("respuesta");

function mensaje(){
    const nac = 2023-parseInt(edad.value);

    respuesta.innerHTML = "Su fecha de nacimiento es: " + nac;
    edad.value="";
}

edad.addEventListener("keydown",(event)=>{
    if (event.key==="Enter"){
        mensaje();
    }
});

boton.addEventListener("click", mensaje);
