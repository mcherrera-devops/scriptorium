---
title : Navegación con enlaces en HTML
description: Desafía tus habilidades creando una navegación clara, utilizando enlaces para conectar con otras secciones de la página y con recursos externos.
svg: draws/anchor-documents.svg
---


```md
## Descripción

Crea una página HTML cuyo objetivo principal sea **trabajar con enlaces (<a>)**.

La página debe simular un **contenido navegable**, donde los enlaces permitan:

- Moverse entre distintas partes del mismo documento
- Conectar secciones relacionadas
- Apuntar a recursos externos

![Demo reto]({{ site.url }}{{ site.baseurl }}/assets/images/demo-reto-enlaces.webp)

El contenido es libre (puede ser sobre un proyecto, una guía, un sitio personal, retos, etc.), pero los enlaces deben **tener un propósito real de navegación**, no estar puestos solo como ejemplo.
```
{:file='enunciado'}

## Boilerplate

Usa **únicamente este HTML inicial** y construye el resto desde cero:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Reto 02</title>
  </head>
  <body>

  </body>
</html>
```
{:file='index.html'}

<details markdown="1" class="container-solution" style="display: none;">
  <summary>Ver solución</summary>

## 1. Header

En la parte superior de la página podemos agrupar el título principal y una pequeña descripción del contenido utilizando la etiqueta **`<header>`**. Esto ayuda a que el usuario entienda rápidamente de qué trata la página.

```html
<header>

  <h1>Guía de recursos para aprender desarrollo web</h1>

  <p>
    En esta página encontrarás distintas secciones con recursos,
    enlaces internos para navegar dentro del documento y enlaces
    externos hacia sitios útiles para aprender programación.
  </p>

</header>
```
{:file="index.html"}

## 2. Menú de navegación con enlaces internos

Podemos crear un pequeño menú utilizando **enlaces internos** que apunten a diferentes secciones del mismo documento. Para ello usamos el atributo **`href="#id"`** que conecta con el **`id`** de cada sección. Estos enlaces permiten **navegar rápidamente dentro de la misma página**.

```html
<nav>

  <ul>
    <li><a href="#html">Recursos HTML</a></li>
    <li><a href="#css">Recursos CSS</a></li>
    <li><a href="#javascript">Recursos JavaScript</a></li>
    <li><a href="#contacto">Contacto</a></li>
  </ul>

</nav>
```
{:file="index.html"}

## 3. Secciones con contenido y enlaces relacionados

Dentro del contenido principal utilizaremos **`<main>`** y varias **secciones (`<section>`)**. Cada sección tendrá un **`id`** para que los enlaces internos puedan apuntar correctamente.

```html
<main>

  <!-- Sección sobre HTML -->
  <section id="html">

    <h2>Recursos para aprender HTML</h2>

    <p>
      HTML es el lenguaje que permite estructurar el contenido de las páginas web.
      Si quieres aprender más, puedes visitar la documentación oficial.
    </p>

    <p>
      <a href="https://developer.mozilla.org/es/docs/Web/HTML">
        Ver documentación de HTML en MDN
      </a>
    </p>

  </section>

  <!-- Sección sobre CSS -->
  <section id="css">

    <h2>Recursos para aprender CSS</h2>

    <p>
      CSS permite aplicar estilos y diseñar la apariencia visual de una página web.
    </p>

    <p>
      <a href="https://developer.mozilla.org/es/docs/Web/CSS">
        Guía completa de CSS
      </a>
    </p>

  </section>

  <!-- Sección sobre JavaScript -->
  <section id="javascript">

    <h2>Recursos para aprender JavaScript</h2>

    <p>
      JavaScript añade interactividad a las páginas web, permitiendo crear
      aplicaciones dinámicas.
    </p>

    <p>
      <a href="https://developer.mozilla.org/es/docs/Web/JavaScript">
        Aprender JavaScript en MDN
      </a>
    </p>

  </section>

</main>
```
{:file="index.html"}


## 4. Footer con enlaces adicionales

Finalmente, podemos incluir un **`<footer>`** con enlaces de contacto o navegación adicional. Esto suele colocarse al final del documento.

```html
<footer id="contacto">

  <h3>Contacto</h3>

  <p>
    Si quieres conocer más recursos sobre desarrollo web,
    puedes visitar los siguientes enlaces:
  </p>

  <ul>
    <li><a href="https://github.com/">GitHub</a></li>
    <li><a href="https://stackoverflow.com/">Stack Overflow</a></li>
    <li><a href="#top">Volver al inicio</a></li>
  </ul>

</footer>
```
{:file="index.html"}

## 5. Ejemplo completo

A continuación se muestra un ejemplo simple de cómo podría quedar la página completa:

```html
<header>
  <h1>Guía de recursos para aprender desarrollo web</h1>
  <p>Explora distintas secciones con enlaces útiles.</p>
</header>

<nav>
  <ul>
    <li><a href="#html">HTML</a></li>
    <li><a href="#css">CSS</a></li>
    <li><a href="#javascript">JavaScript</a></li>
    <li><a href="#contacto">Contacto</a></li>
  </ul>
</nav>

<main>

  <section id="html">
    <h2>HTML</h2>
    <p>Lenguaje base para estructurar páginas web.</p>
    <a href="https://developer.mozilla.org/es/docs/Web/HTML">
      Documentación de HTML
    </a>
  </section>

  <section id="css">
    <h2>CSS</h2>
    <p>Lenguaje para aplicar estilos y diseño visual.</p>
    <a href="https://developer.mozilla.org/es/docs/Web/CSS">
      Guía de CSS
    </a>
  </section>

  <section id="javascript">
    <h2>JavaScript</h2>
    <p>Lenguaje que permite añadir interactividad.</p>
    <a href="https://developer.mozilla.org/es/docs/Web/JavaScript">
      Guía de JavaScript
    </a>
  </section>

</main>

<footer id="contacto">
  <h3>Contacto</h3>
  <ul>
    <li><a href="https://github.com/">GitHub</a></li>
    <li><a href="https://stackoverflow.com/">Stack Overflow</a></li>
    <li><a href="#top">Volver arriba</a></li>
  </ul>
</footer>
```
{:file="index.html"}

</details>