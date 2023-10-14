---
layout: ../../layouts/MarkdownPostLayout.astro
title: Inicios en Godot
author: Rojo Fang
description: "Este es el inicio de un proyecto en Godot."
image:
  url: "../../godot_logo.svg"
  alt: "Capturas de pantalla del software Godot"
pubDate: 2023-10-03
tags: ["Video Games", "3D", "Godot"]
---

# GODOT

# [🕹️]

## INICIEMOS UN PROYECTO NUEVO GODOT

- Creamos un Nodo3D con una cámara 3D dentro.

![Imagen de motor gráfico para el desarrollo de videojuegos GODOT](/img-post-uno/node-camera.svg "Creación de Nodo3D")

- En la parte superior del programa, podemos observar tres puntos en disposición vertical.

![Imagen de motor gráfico para el desarrollo de videojuegos GODOT](/img-post-uno/navegacion.png "Creación de Nodo3D")

- Al hacer clic sobre ellos, se despliega un menú que posee un botón que dice `Add Sun To Scene`, con el cual agregamos un sol. Hacemos clic en él.

![Imagen de motor gráfico para el desarrollo de videojuegos GODOT](/img-post-uno/creacion-de-sol.png "Creacion de Sol")

- Volvemos a hacer clic sobre los puntos y clic en el botón que dice: `Add environment To Scene`, agregando un ambiente.

![Imagen de motor gráfico para el desarrollo de videojuegos GODOT](/img-post-uno/entorno-de-escena.png "Creacion de entorno")

- Con esto ya podemos reproducir nuestra escena ![Imagen de motor gráfico para el desarrollo de videojuegos GODOT](/img-post-uno/escena.png) en el panel de la esquina superior derecha. O con la tecla F6. Le ponemos un nombre a la escena y la guardamos.

## MESH INSTANCE 3D

- En la escena principal, agregamos un nuevo nodo. Este nodo lo podemos agregar haciendo clic en el icono `+` que se encuentra hacia la izquierda superior de nuestra pantalla. En el buscador del menú que nos aparece escribimos `meshin` y se nos da a elegir algunos tipos de nodo. Seleccionamos `MeshInstance3D` y damos crear.

![Imagen de motor gráfico para el desarrollo de videojuegos GODOT](/img-post-uno/meshin.png "Mesh instance 3D")

- Ahora podemos verlo dentro de la jerarquía de nuestra escena.

![Imagen de motor gráfico para el desarrollo de videojuegos GODOT](/img-post-uno/meshin-escena.png "Mesh instance 3D")

- Hacia la derecha de nuestra pantalla nos encontramos con el inspector, que como tiene seleccionado nuestro nodo `MeshInstance3D`, nos muestra sus propiedades. Hacemos clic en `<empty>` y agregamos un `Nuevo PlaneMesh`.

![Imagen de motor gráfico para el desarrollo de videojuegos GODOT](/img-post-uno/empty.png)

- En el inspector podemos observar la propiedad size a la cual le cambiamos el valor a x:10m e y:10m.

> Nótese que si volvemos a reproducir la escena, el plano todavía no se ve. Esto se debe a que la malla y la cámara se encuentran sobre la misma línea del horizonte.

- Seleccionamos la cámara (en la pantalla podemos observar un icono rojo con forma de cámara si hacemos clic en él podemos obtener una vista rápida de la cámara).

- Una vez seleccionada la cámara, veamos el inspector. En la barra de navegación vamos a nodo 3 ingresamos a su transform y cambiamos el valor del eje y de `0.65` a `2` y reproducimos nuevamente la escena con `F6`.

## CONFIGURACIÓN GRÁFICA

- En la esquina superior izquierda de la pantalla, hacemos clic en `Proyecto` y luego en `ajustes del proyecto`. En la pestaña `general`, vamos a `display` y a `Windows`. Dentro en `Size`, ajustamos los valores de `Viewport Height en 1920` y los de `Viewport Width en 1080`, luego en `Modo` colocamos `Maximized`.

- Una vez hecho esto, en la columna de la izquierda de la pestaña `general`, localizamos Rendering y hacemos clic en Anti Aliasing. En `Quality MSAA 3D`, colocamos la opción de `2x (Average)`. Luego hacemos clic en `Advanced Settings`. Nuevamente en el panel de la izquierda buscamos, en este caso, `Lights and Shadows`, hacemos clic, buscamos `Directional Shadows` y `Soft Shadows Filter` y colocamos la opción de `Soft Medium (Average)`.

## CREACIÓN DEL PERSONAJE

- Colocamos nuestra vista sobre la esquina superior izquierda de la pantalla. Vamos a `Escena` `Nueva escena`.

- Ingresamos a nuestra nueva escena y en el panel de izquierdo donde dice Escena, hacemos clic en el botón `+ Other node` en la tarjeta que nos aparece en la pantalla, ingresamos en el buscador la palabra `body3d` dándonos como resultado una lista de la cual tenemos que elegir el nodo `RigidBody3D` y damos `Create` en el botón que se encuentra en la `parte inferior` de la tarjeta.

- Hacemos clic sobre el nodo creado y le cambiamos el nombre a `Player`. Una vez hecho esto, damos en crear nuevo nodo con el signo de `+`, en el buscador escribimos `meshins` y seleccionamos la opción de `MeshInstance3D` y luego en create. Esto nos da como resultado un `nuevo nodo hijo` de `Player`.

- En las propiedades del `MeshInstance3D` en el `Inspector`, podemos observar que en las propiedades en la sección de `Mesh`, dice `<empty>`, damos clic dentro y seleccionamos la opción `New CapsuleMesh`. Una vez creada la malla, en la parte superior del programa, podemos observar un icono cuadrado rojo que dice `Mesh`. Hacemos clic en él y seleccionamos `Crear collider conexo hermano`.

- Una vez hecho esto, hacemos clic en el `nodo padre` `Player` y en el inspector buscamos la opción `Lock Rotation` y la activamos haciendo clic en el `checkbox`.
