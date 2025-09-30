# Proyecto: Explorando la Política Fiscal de Colombia 🏴‍☠️

¡Bienvenidos al repositorio del juego desarrollado en Roblox studio! Vamos a una aventura motivada por el conocimiento de conceptos clave de la política fiscal, específicamente del Marco Fiscal de Mediano Plazo (MFMP) 2025.

## Descripción del Juego

En este juego, los jugadores exploran un archipiélago pirata en busca de tesoros. Cada cofre que encuentran no contiene oro, ¡sino una pregunta de opción múltiple sobre el gasto público y el MFMP!

* **Respuesta Correcta:** El jugador es recompensado y puede continuar su aventura.
* **Respuesta Incorrecta:** Se activan castigos divertidos y desafiantes, como explosiones o gases tóxicos, que deben superar para seguir adelante.

## Estado Actual del Proyecto (Commit: [Fecha Actual, ej: 29/09/2023])

Este primer *commit* representa la base del sistema de preguntas y respuestas. He logrado completar los siguientes puntos:

* **Estructura de Datos:** He creado un **`ModuleScript`** (`DatosFiscales`) que contiene un catálogo de preguntas, opciones y las respuestas correctas. Esto me permitirá añadir fácilmente más preguntas en el futuro.
* **Canal de Comunicación:** He establecido un **`RemoteEvent`** (`EventoPregunta`) para la comunicación segura entre el servidor y el cliente.
* **Interfaz de Usuario (GUI):** He diseñado la estructura visual en **`StarterGui`** (`PreguntasFiscalesGUI`) que servirá para mostrar las preguntas y las opciones de respuesta a los jugadores.

## Próximos Pasos

En la siguiente fase, me enfocaré en:

1.  Implementar la **lógica del cofre** en un `Script` para que, al tocarlo, se active la GUI de preguntas.
2.  Configurar los **castigos** para que funcionen correctamente.
3.  Añadir más preguntas al `ModuleScript`.

¡Gracias por seguir el progreso de este proyecto!
