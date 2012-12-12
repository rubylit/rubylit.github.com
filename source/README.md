rubylit.github.com
==================

Esta es la nueva página para rubylit.org.ar

## ¿Que queremos lograr con ésta página? ##

- Queremos tener un lugar donde podamos ir subiendo los slides de las meetups.
- Tener una página de presentación del grupo.
- Tener una página para invitar a las meetups y las conferencias.

## ¿Queremos reemplazar la wiki existente? ##

El problema de la wiki actual es el spam, solucionado ese tema, podriamos
perfectamente usarlo, sino se puede solucionar podriamos instalar otro sistema.

## ¿Cómo se puede modificar esta página? ¡está horrible! ##

Bueno, hay varias cosas a tener en cuenta, la página está hecha usando
[octopress] [1] cosa que deberían tener en cuenta! La rama que deben modificar
es la rama `source` **no master!**.

Entonces, para cambiar los estilos, clonan el repositorio, van a la rama source
y modifican los directorios `sass` y `source`.

Para modificar este readme modifican el archivo `source/README.md`.

Para crear un post, usan la tarea de `rake new_post[titulo]`.

Para ver como queda, usan la tarea de `rake preview`

Para publicar los cambios (hacer push) tienen que:

1. Commitear y hacer push de la rama `source`.
2. Usar la tarea de `rake deploy`.



