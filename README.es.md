# SamSho Reader

[English](README.md) · **Español** · [Deutsch](README.de.md) · [Français](README.fr.md) · [Italiano](README.it.md) ·
[Português (Brasil)](README.pt-BR.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

Un mod de lector de pantalla para **SAMURAI SHODOWN** (2019; Steam, PC). Lee los menús, la historia, las listas de comandos, las tablas y el texto en pantalla con el lector de pantalla que ya usas (NVDA, JAWS), en el idioma en que está el juego.

Autor: Bruno Broiero, con ayuda de Claude.

## Qué hace

- Menú principal y todos los submenús, con la descripción de cada entrada.
- Opciones: juego, pantalla, sonido (volúmenes en %), idioma y subtítulos, botón config (cada acción con su tecla o botón).
- Selección de personaje, incluidos aleatorio, trajes y colores; escenarios; asignación de lados en Versus.
- Historia: subtítulos y diálogos, desbloqueos, epílogo y créditos.
- Tutorial: instrucción, tarea y mensaje final, con las teclas en palabras.
- Lista de comandos: cada movimiento con su comando en la notación que elijas; recorrida con el stick o F2 / F3.
- Pausa y ajustes de Entrenamiento.
- Base de datos: perfil, rankings propios, registros generales.
- Galería: películas, ilustraciones, voces y música, con sus pestañas y páginas.
- Online: marcadores, pantallas de batalla clasificada y relajada, listas de sombras de Batalla Fantasma.
- Resultados: la frase del ganador se lee sola; el puntaje queda retenido y lo pedís con el stick o F1.
- Carteles de desbloqueo y avisos.

No se lee:

- La pantalla de felicitación al terminar la historia es un dibujo sin texto.
- Las salas y el chat del online no se probaron con rivales.

## Instalación

Se necesita la versión de Steam para PC de SAMURAI SHODOWN, Windows x64 y un lector de pantalla en marcha (NVDA o JAWS). UE4SS, el cargador de mods para juegos Unreal, viene dentro del zip, en la versión que funciona con este juego.

Extrae todo el contenido del zip en `SamuraiShodown\Binaries\Win64` (en Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, la carpeta `ue4ss` y estos README.

Inicia el juego desde Steam, no desde el .exe: sin Steam arranca en inglés y sin conexión. El mod dice "SamSho Reader" en cuanto está funcionando; si no lo oyes, F8 dice el nombre del lector de pantalla que encontró. No se modifica ningún archivo del juego.

Para desinstalar, borra `dwmapi.dll` y la carpeta `ue4ss`. UE4SS y PRISM, la biblioteca que habla con el lector de pantalla, se distribuyen con sus propias licencias: ver `THIRD-PARTY.md`.

## Teclas

Fuera de una pelea:

| Tecla | Mando | Qué hace |
|---|---|---|
| F1 | Stick derecho izquierda o derecha | Dice todo lo retenido (una lista de comandos, una tabla, un resultado) |
| F2 / F3 | Stick derecho arriba / abajo | Pieza anterior / siguiente de lo retenido |
| F10 | Clic del stick derecho | Cambia la notación de los comandos (Normal, Arcade, Arcade simplificado, FGC, FGC simplificado). La elección se guarda |
| F4 | Clic del stick derecho, si no hay nada retenido | Lee la leyenda de botones de la pantalla ("9 o A Confirmar, 0 o B Volver") |

En una pelea:

Nada habla solo: la pelea ya se oye. Con el stick derecho pedís el dato que necesitás:

| Stick derecho | Dice |
|---|---|
| Izquierda | Vida de los dos lados: "vida 71%, 80%" (primero tu lado) |
| Arriba | Furia: "furia 41%, máxima" |
| Abajo | Rondas ganadas: "RONDAS 1, 0". En Supervivencia, Contrarreloj e Ironman, tus victorias seguidas |
| Derecha | Tiempo del round |
| Clic | Todo junto |

Teclado: F2 vida, F3 furia, F10 rondas, F1 todo.

En Supervivencia, Contrarreloj e Ironman solo se dice tu lado.

Siempre:

| Tecla | Mando | Qué hace |
|---|---|---|
| F6 | L3 + R3 (los dos sticks apretados a la vez) | Apaga el mod y lo vuelve a prender; lo confirma con las palabras del juego para activado y desactivado. No se guarda: siempre arranca prendido |
| F8 | | Dice qué lector de pantalla usa el mod |

## Qué leen F1, F2, F3 y el stick derecho

Muchas pantallas muestran más de lo que hay bajo el cursor: una lista de comandos, los puntajes de un resultado, una tabla de registros, una lección. El mod no lee todo eso al llegar: lo guarda y lo entrega con estas teclas: F3 avanza una pieza, F2 vuelve a la anterior y F1 lo dice todo de una vez. Al llegar al final, F3 no dice nada: así se sabe que no hay más. En el mando, el stick derecho hace lo mismo: abajo es F3, arriba es F2, izquierda o derecha es F1.

Qué es una pieza depende de la pantalla:

- **Lista de comandos**: cada movimiento con su comando, en la notación elegida con F10 o el clic del stick; al cambiarla, el movimiento se repite en la nueva. Al entrar se dicen el personaje y la categoría.
- **Tutorial**: cada frase de la explicación y de la tarea, con las entradas puestas en palabras; el clic también cambia su notación.
- **Resultado**, al terminar una pelea: la frase del ganador se dice sola; los puntajes esperan en las teclas, a propósito, para que la frase no quede enterrada bajo las cifras.
- **Resultado de versus**: victorias, derrotas, empates, porcentaje y puntos de cada lado.
- **Datos del jugador**: las tablas de registros y rankings, una fila por pieza; al llegar se dicen el título y la primera fila.
- **Leyenda de botones**: sin nada guardado, el clic del stick (o F4) lee la leyenda de botones de la propia pantalla.

## La lista de comandos y sus notaciones

En el juego, un comando es una fila de dibujos: flechas, botones, un "más", condiciones. El mod los pasa a palabras, y como cada jugador viene de un lugar distinto (la sala de arcade, los foros, o ninguno), ofrece cinco formas de decirlos. Se cambia con F10 o el clic del stick derecho, y la elección queda guardada. El mismo comando, cuarto de círculo adelante y corte fuerte, en cada una:

| Notación | Cómo suena |
|---|---|
| Normal | abajo, diagonal abajo adelante, adelante más Corte H |
| Arcade | cuarto de círculo adelante, Corte H |
| Arcade simplificado | cuarto de círculo adelante, C |
| FGC | 2 3 6, Corte H |
| FGC simplificado | 2 3 6, C |

- **Normal** dice cada dirección con su palabra. Es la más larga y la que no supone nada.
- **Arcade** nombra la figura: cuarto de círculo, medio círculo, dragon punch, y sus inversos. Es como se dicen los comandos de viva voz.
- **FGC** usa los números del teclado numérico, la notación de la comunidad: 6 es adelante, 2 abajo, 3 la diagonal de abajo adelante; siempre mirando a la derecha.
- Las variantes **simplificadas** cambian los nombres de los botones por las letras del gabinete: A corte ligero, B medio, C fuerte, D patada.

Cómo se pensó la lectura, porque un dibujo dice cosas con su forma que las palabras tienen que decir en voz alta:

- Una diagonal es un solo movimiento, así que se llama "diagonal": "abajo, diagonal abajo adelante, adelante". Dicho como "abajo, abajo adelante, adelante" no se sabe si son dos entradas o una.
- Dos botones dibujados pegados se pulsan juntos, así que van con "más" en todas las notaciones.
- Una condición que el juego dibuja alrededor del nombre del movimiento ("durante ~") se dice una vez, no en dos mitades.
- Una condición como "repetidamente" se dice después de los botones a los que afecta: "adelante más Corte L, repetidamente", que es como se dice, no como se dibuja.
- Los nombres de los botones y de las condiciones son las palabras del juego, sacadas de la leyenda de su propia lista de comandos; las direcciones, las figuras, "más" y "o" son del mod, en los once idiomas.
- "O" tiene varias formas en el juego (dos botones alternativos, dos comandos, una lista); todas se dicen con la misma palabra.

La lista se recorre con el stick derecho (arriba y abajo, movimiento por movimiento; izquierda o derecha, entera) o con F2, F3 y F1. Al entrar se dice el peleador y la categoría ("SHIKI, MOVIMIENTOS ESPECIALES") y después cada movimiento como "nombre, condición si tiene: comando", por ejemplo "Elysium Halo: adelante, abajo, diagonal abajo adelante más Corte L o Corte M o Corte H".

## Informar un problema

Cierra el juego normalmente y envía `SamuraiShodown\Binaries\Win64\ue4ss\UE4SS.log`: registra lo que el juego mostró y lo que el mod dijo al respecto, con las palabras exactas, así que no hace falta anotar lo que escuchaste. Indica en qué pantalla fue y qué esperabas oír.

## Compilar

El mod es Lua, cargado por UE4SS; no se compila nada salvo `prism_bridge.dll`, el pequeño módulo nativo que entrega la voz a PRISM y lee el mando (`native\prism_bridge\build.ps1`, requiere MSVC). `python tools\package.py` arma el zip de la release desde la carpeta del juego.

## Traducciones

Este README se publica en todos los idiomas que admite el juego. Solo el inglés y el español fueron revisados por un hablante; se agradecen correcciones a los demás. El mod habla en el idioma del juego: casi todo lo que dice es texto del propio juego, y sus pocas palabras propias (direcciones, nombres de teclas, "vida", "furia") solo fueron verificadas de oído en español.
