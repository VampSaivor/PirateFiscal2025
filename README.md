# Proyecto: Explorando la Política Fiscal de Colombia 🏴‍☠️

¡Bienvenidos al repositorio del juego desarrollado en Roblox studio! Vamos a una aventura motivada por el conocimiento de conceptos clave de la política fiscal, específicamente del Marco Fiscal de Mediano Plazo (MFMP) 2025.

## Descripción del Juego

En este juego, los jugadores exploran un archipiélago pirata en busca de tesoros. Cada cofre que encuentran no contiene oro, ¡sino una pregunta de opción múltiple sobre el gasto público y el MFMP!

* **Respuesta Correcta:** El jugador es recompensado y puede continuar su aventura.
* **Respuesta Incorrecta:** Se activan castigos divertidos y desafiantes, como explosiones o gases tóxicos, que deben superar para seguir adelante.

## Estado Actual del Proyecto (Commit: [Fecha Actual, 29/09/2025])

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

# Proyecto: Explorando la Política Fiscal de Colombia 🏴‍☠️

¡Bienvenidos al repositorio de mi primer juego en Roblox! Este proyecto busca combinar la diversión de una aventura de piratas con el aprendizaje de conceptos clave de la política fiscal colombiana, específicamente del Marco Fiscal de Mediano Plazo (MFMP) 2025.

## Descripción del Juego

En este juego, los jugadores exploran un archipiélago pirata en busca de tesoros. Cada cofre que encuentran no contiene oro, ¡sino una pregunta de opción múltiple sobre el gasto público y el MFMP!

* **Respuesta Correcta:** El jugador es recompensado y puede continuar su aventura.
* **Respuesta Incorrecta:** Se activan castigos divertidos y desafiantes, como explosiones o gases tóxicos, que deben superar para seguir adelante.

---

## Estado Actual del Proyecto (Funcionalidad V1 - 30/09/2025)

Hemos completado la funcionalidad principal del juego, permitiendo que un jugador active el cofre, reciba una pregunta en la GUI y sea castigado/recompensado según su respuesta.

**Logros de esta Fase:**

1.  **Lógica del Cofre Completada:**
    * Se implementó el **`ScriptServidor`** (`CofrePregunta1`) que usa el evento `Touched` del **`Hitbox`** para detectar jugadores y asignarles una pregunta.
    * **Corrección de Errores Críticos:** Se solucionó el error de serialización (`Dictionary is not a supported attribute type`) utilizando el servicio **`HttpService`** (`JSONEncode` / `JSONDecode`) para pasar correctamente los datos de la pregunta entre el servidor y el cliente.
2.  **Sistema de Preguntas y Comunicación:**
    * El **`LocalScript`** (`ScriptClienteGUI`) recibe la pregunta a través del `RemoteEvent` (`EventoPregunta`) y la muestra correctamente en la interfaz (`PreguntasFiscalesGUI`).
    * Se captura la respuesta del jugador al hacer clic y se envía de vuelta al servidor para verificación.
3.  **Castigos Funcionales:**
    * El servidor verifica la respuesta y aplica el castigo aleatorio (`Explosión`, `Gas Tóxico`, o `Caída en Lava`) definido en el `ModuleScript` (`DatosFiscales`).
    * La recompensa (`player:LoadCharacter()` y destrucción del cofre) se aplica al responder correctamente.

---

## Próximas Tareas

La lógica central está lista. Los siguientes pasos se centrarán en mejorar la experiencia del jugador:

1.  **Diseño y Usabilidad de la GUI:** Mejorar el aspecto visual (`PreguntasFiscalesGUI`) para que sea atractivo y fácil de usar.
2.  **Creación de más Contenido:** Añadir al menos 5 preguntas más al `ModuleScript` sobre el MFMP 2025.
3.  **Mejora de Castigos:** Implementar el castigo de aparición de enemigos (spawn de un `Zombie` simple).
4.  **Progresión:** Crear un segundo cofre (`CofrePregunta2`) y usar la destrucción
