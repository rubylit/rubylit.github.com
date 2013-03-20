rubylit.github.com
==================

Esta es la nueva página para rubylit.org.ar

## ¿Que queremos lograr con ésta página? ##

- Tener un lugar donde podamos ir subiendo los slides de las meetups.
- Tener una página de presentación del grupo.
- Tener una página para invitar a las meetups y las conferencias.

## ¿Queremos reemplazar la wiki existente? ##

El problema de la wiki actual es el spam, solucionado ese tema, podriamos
perfectamente usarlo, sino se puede solucionar podriamos instalar otro sistema.

## ¿Cómo se puede modificar esta página? ¡está horrible! ##

Bueno, hay varias cosas a tener en cuenta, la página está hecha usando
[octopress](http://octopress.org/docs/) por lo tanto la rama que deben modificar
es la rama `source` **no master!**.

Para cambiar los estilos, clonan el repositorio, van a la rama source
y modifican los directorios `sass` y `source`.

Para modificar este readme modifican el archivo `source/README.md`.

## ¿Cómo genero un nuevo post?

Para crear un post, usan la tarea de

`rake new_post[titulo]`

Esto crea un archivo dentro de la carpeta `source/_posts` con el nombre
`YYYY-MM-DD-post-title.markdown` de acuerdo con las convenciones de Jekyll

El archivo tendrá esta forma

```ruby
---
layout: post
title: "Titulo"
date: YYYY-MM-DD
comments: true
categories:
---

```
Debajo de estas lineas pueden empezar a escribir usando markdown. Tambien pueden
ver los posts anteriores, que se encuentran en el mismo directorio, para guiarse.

Para ver como queda, usan la tarea

`rake preview`

Para publicar los cambios (hacer push) tienen que:

1. Commitear y hacer push de la rama `source`.
2. Usar la tarea de `rake deploy`.
