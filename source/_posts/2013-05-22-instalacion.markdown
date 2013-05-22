---
layout: post
title: "Instalando RoR"
date: 2013-05-22 09:36
comments: true
categories: [RubyStation, instalación]
author: olvap
---

La idea de este post es, mediante una serie de pasos, tener registrado el proceso de instalación de ruby y Ruby on rails.

## Ubuntu

### Dependencias necesarias.

En la terminal
    sudo apt-get install autoconf automake bison build-essential curl git-core libapr1 libaprutil1 libc6-dev libltdl-dev libreadline6 libreadline6-dev libsqlite3-0 libsqlite3-dev libssl-dev libtool libxml2-dev libxslt-dev libxslt1-dev libyaml-dev ncurses-dev openssl sqlite3 zlib1g zlib1g-dev


## Windows

Desde RubyLit no aconsejamos usar Windows, pero si realmente no te queda otra, podes bajarte un instalador en esta [página][1]

## Git

Es un [sistema de control de versiones][6], pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente.

[GitHub][3], es un sitio web para compartir proyectos en git. Si todavía no tenes cuenta, hacela ya que la mayoria del código de [ruby][4] y [rails][5] está en esta web.

## RVM

[RVM][2] es una herramienta de consola que nos permite fácilmente instalar, administrar, y trabajar con multiples entornos de ruby desde interpretes hasta sets de gemas.

Para instalar la última version ejecutamos en la consola.

    curl -L get.rvm.io | bash -s stable

Cerramos la consola y la brimos nuevamente. Para verificar que todo esté en orden escribimos esto en la terminal.

    type rvm | head -1

Tiene que devolver algo así:

    rvm is a function

Si escribimos.

    rvm -v

Vamos a ver algo parecido a esto.

    rvm 1.x.x (stable) by ...

Si estás usando Ubuntu 12.04 o la última version de Mint, asegurate de tener la opcion 'Run command as login shell' marcada en la pestaña 'Title and Command' en Profile Preferences. Despues de cambiar esto, vas a tener que reiniciar la consola para que los cambios tengan efecto.

## Ruby

ahora que tenemos instalado rvm en nuestra computadora, podemos instalar cualquier version de ruby.
Probamos con

    rvm install 1.9.3

Dejamos como default con --default

    rvm use 1.9.3 --default

## Rails

Para instalar rails, simplemente tenemos que correr esto en la terminal

    gem install rails

para verificar que está todo bien podemos intentar crear una aplicación rails con el comando

    mkdir proyects
    cd proyects
    rails new prueba

Tenemos que ver una salida con los archivos creados.

[1]: http://railsinstaller.org/
[2]: https://rvm.io/
[3]: https://github.com/
[4]: https://github.com/ruby/ruby
[5]: https://github.com/rails/rails
[6]: http://es.wikipedia.org/wiki/Control_de_versiones
