---
title: "Crear un CV semántico en HTML"
description: Crea tu currículum en **HTML usando etiquetas semánticas**, estructurando correctamente la información y aplicando buenas prácticas desde el inicio.
svg: draws/cv-html.svg
solutions: true
---

```md
## Objetivo

El objetivo de este reto es que practiques la **estructura básica de un documento HTML semántico** mientras comienzas a crear un **Currículum Vitae (CV) digital**.

Vas a enfocarte en organizar el documento correctamente usando las etiquetas esenciales de HTML antes de preocuparte por estilos o contenido detallado. Esto te permitirá construir un CV claro, accesible y con buena estructura desde cero.

![Demo CV]({{ site.url }}{{ site.baseurl }}/assets/images/demo-reto-html-cv.webp)

## Indicaciones

1. Crea un archivo HTML dentro de tu carpeta de trabajo (**index.html** o similar).
2. Puedes usar un editor de código o una plataforma en línea como CodePen.
3. El contenido y las secciones del CV deberán estar estructuradas usando etiquetas semánticas.
4. Asegúrate de que la página se renderice correctamente en el navegador.
```
{:file="enunciado"}

## Boilerplate

Usa **únicamente este HTML inicial** y construye el resto desde cero:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <title>Mi CV</title>
  </head>
  <body>
    <!-- 1. Header: aquí va tu nombre y perfil breve -->
    <!-- 2. Sección de Perfil profesional -->
    <!-- 3. Sección de Experiencia laboral -->
    <!-- 4. Sección de Educación -->
    <!-- 5. Footer: información de contacto -->
  </body>
</html>
```
{:file='index.html'}

<details markdown="1" class="container-solution" style="display: none;">
  <summary>Ver solución</summary>

## 1. Header

En la parte principal del CV agruparemos el título, la foto de perfil y el nombre de la persona, usando como contenedor la etiqueta **`<header>`**.

```html
<header style="text-align: center;">
  <h1>Curriculum Vitae</h1>
  <img src="https://i.ibb.co/SXnSFrkB/profile.png" width="80" height="80" alt="cv photo">
  <h2>JUAN PERÉZ</h2>
</header>
```
{:file="index.html"}

## 2. Secciones del curriculum

Dentro del contenido principal trabajaremos principalmente con secciones (**`<section>`**) para cada apartado, como la formación académica, la experiencia y la información complementaria, entre otros. Un ejemplo de esta estructura sería el siguiente:

```html
<header> ... </header>

<main>
  <!-- Sección 1: por ejemplo, Formación académica -->
  <section>
    <h3>Título</h3>
    <p>Párrafo</p>
    <blockquote>Notas</blockquote>
    <ul></ul>
  </section>

  <!-- Sección 2: por ejemplo, Experiencia laboral -->
  <section>
    ....
  </section>

  <!--
    A partir de aquí puedes seguir agregando más secciones
    según los apartados de tu CV, por ejemplo:
    - Información complementaria
    - Habilidades
    - Idiomas
    - Proyectos
  -->

</main>
```
{:file="index.html"}

## 3. Footer y datos de contacto

Finalmente, al término del contenido principal del currículum, podemos utilizar la etiqueta **`<footer>`** para incluir la información de contacto. Esta sección suele ubicarse después del **`<main>`** y agruparemos los datos de contacto.

```html
<main> ... </main>

<!-- Footer del currículum -->
<footer>

  <h3>Datos de contacto</h3>

  <p>Email: correo@ejemplo.com</p>
  <p>Teléfono: +56 9 1234 5678</p>

  <!-- Enlaces a perfiles profesionales -->
  <ul>
    <li><a href="#">LinkedIn</a></li>
    <li><a href="#">GitHub</a></li>
    <li><a href="#">Portafolio</a></li>
  </ul>

</footer>
```
{:file="index.html"}

## 4. Ejemplo completo

A continuación, se muestra un ejemplo completo de cómo podría quedar:

```html
<header>
  <h1>Currículum Vitae</h1>
  <img src="https://i.ibb.co/SXnSFrkB/profile.png" alt="Foto de perfil">
  <h2>Juan Pérez</h2>
</header>

<main>

  <section>
    <h3>Perfil profesional</h3>
    <p>
      Desarrollador web con interés en tecnologías modernas y buenas prácticas
      de programación. Experiencia en desarrollo frontend y backend.
    </p>
  </section>

  <section>
    <h3>Experiencia laboral</h3>
    <ul>
      <li>
        <strong>Empresa ABC</strong> – Desarrollador Web (2022 - Actualidad)
        <p>Desarrollo de aplicaciones web utilizando JavaScript y Python.</p>
      </li>
      <li>
        <strong>Empresa XYZ</strong> – Soporte TI (2020 - 2022)
        <p>Mantenimiento de sistemas y soporte técnico a usuarios.</p>
      </li>
    </ul>
  </section>

  <section>
    <h3>Educación</h3>
    <ul>
      <li>Ingeniería en Informática – Instituto Ejemplo</li>
      <li>Curso de Desarrollo Web – Plataforma Online</li>
    </ul>
  </section>

</main>

<footer>
  <h3>Contacto</h3>
  <ul>
    <li>Email: juan@example.com</li>
    <li>Teléfono: +56 9 1234 5678</li>
    <li>GitHub: github.com/juanperez</li>
  </ul>
</footer>
```
{:file="index.html"}

</details>