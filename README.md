# AviGuess 🐦

AviGuess es un juego de deducción diario en el navegador, inspirado en mecánicas tipo Wordle, pero diseñado para los amantes de la ornitología.
El objetivo es adivinar el ave oculta en un máximo de 10 intentos utilizando pistas de proximidad taxonómica y atributos biológicos.


## ✨ Características Principales

* **Dos Modos de Juego:**
  * **📅 Modo Diario:** Un reto único cada día, sincronizado globalmente para todos los jugadores. Incluye contador de rachas y persistencia si cierras la pestaña a mitad de partida.
  * **🔁 Modo Práctica:** Genera aves aleatorias para jugar de forma ilimitada.
* **Proximidad Filogenética:** Un sistema de pistas avanzado que calcula el porcentaje de parentesco entre el intento del usuario y el ave objetivo basándose en su Orden y Familia evolutiva.
* **Guía de Campo (Colección):** Una "Pokedex" integrada que guarda localmente las especies que has logrado identificar, mostrando su nombre científico, emoji y una curiosidad única.
* **Estadísticas Detalladas:** Seguimiento de partidas jugadas, porcentaje de victorias, rachas y distribución de intentos en un gráfico de barras.
* **Buscador Inteligente:** Campo de texto autocompletable que ignora tildes y sugiere nombres comunes y científicos.
* **Carga Dinámica de Datos:** El juego lee su base de datos directamente desde un archivo CSV alojado en Google Sheets, permitiendo actualizar la lista de aves sin tocar el código fuente.

## 🎮 Cómo Jugar

1. Escribe el nombre de un ave en el buscador para hacer tu primer intento.
2. El juego comparará tu ave con el ave oculta a través de 7 atributos:
   * **Orden** y **Familia** (Taxonomía)
   * **Hábitat**, **Dieta**, **Tamaño**, **Migración** y **Continente**
3. Los colores te indicarán qué tan cerca estás:
   * 🟩 **Verde:** Coincidencia exacta.
   * 🟥 **Rojo:** Sin coincidencia.
4. La **Barra de Proximidad** te dará un porcentaje indicando el parentesco evolutivo entre tu intento y la respuesta.
5. ¡Tienes 10 intentos para descubrir la especie correcta! (Al quinto intento fallido, recibirás una pista extra).

## 🛠️ Tecnologías y Arquitectura

Este proyecto está construido sin frameworks externos para mantenerlo ligero y rápido:

* **HTML5 / CSS3:** Interfaz 100% responsiva (Mobile First) con diseño en modo oscuro (Dark Mode).
* **Vanilla JavaScript:** Toda la lógica del juego, motor de búsqueda, y cálculos filogenéticos.
* **LocalStorage API:** Para la persistencia del progreso diario, estadísticas y colección de la Guía de Campo.
* **Fetch API & CORS Proxies:** Para consumir de forma asíncrona la base de datos alojada en Google Sheets.
