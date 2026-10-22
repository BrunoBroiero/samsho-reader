# SamSho Reader

Mod de accesibilidad para **SAMURAI SHODOWN** (2019, Steam): hace que el juego se lea con tu lector de pantalla. Menús, opciones, selección de personaje y escenario, subtítulos de la historia, tutorial, lista de comandos, base de datos, galería, online, resultados y los números de la pelea.

Casi todas las palabras que vas a oír son las del propio juego, en el idioma en que lo tengas configurado. Las pocas palabras que el juego no tiene (direcciones de los comandos, nombres de teclas, "vida", "furia") están traducidas a los once idiomas del juego.

Autor: **Bruno Broiero**. Hecho con Claude.

## Requisitos

- SAMURAI SHODOWN para Steam (Windows).
- Un lector de pantalla en marcha: NVDA o JAWS. El mod habla a través de PRISM.
- [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS), el cargador de mods para juegos Unreal. Viene adentro de la descarga, en la versión que funciona con este juego (experimental, 21 de septiembre de 2026): no hay que bajar nada aparte.
- Un mando XInput (tipo Xbox) es opcional, pero el mod está pensado para él.

## Instalación

1. Bajá el `SamShoReader-x.y.z.zip` más nuevo de la página de Releases.
2. Descomprimí todo lo que trae dentro de `SamuraiShodown\Binaries\Win64\` (la carpeta del juego, en Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, la carpeta `ue4ss` y los README.
3. Abrí el juego **desde Steam** (no desde el .exe: sin Steam arranca en inglés y sin conexión).
4. Al cargar, el mod dice "SamSho Reader". Si no lo oís, apretá F8: dice el nombre del lector de pantalla que encontró.

## Teclas del mod

| Tecla | Mando | Qué hace |
|---|---|---|
| F1 | Stick derecho izquierda o derecha | Dice todo lo retenido (una lista de comandos, una tabla, un resultado) |
| F2 / F3 | Stick derecho arriba / abajo | Pieza anterior / siguiente de lo retenido |
| F10 | Clic del stick derecho | Cambia la notación de los comandos (Normal, Arcade, Arcade simplificado, FGC, FGC simplificado). La elección se guarda |
| F4 | Clic del stick derecho, si no hay nada retenido | Lee la leyenda de botones de la pantalla ("9 o A Confirmar, 0 o B Volver") |
| F7 | | Frena la voz |
| F6 | L3 + R3 (los dos sticks apretados a la vez) | Apaga el mod y lo vuelve a prender; lo confirma con las palabras del juego para activado y desactivado. No se guarda: siempre arranca prendido |
| F8 | | Dice qué lector de pantalla usa el mod |
| Ctrl + Escape | | Calla la voz |

Las flechas, Enter y Backspace son del juego, no del mod.

## En la pelea

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

## Qué se lee

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

## Lo que no se lee

- La pantalla de felicitación al terminar la historia es un dibujo sin texto.
- Las salas y el chat del online no se probaron con rivales.

## Idiomas

El mod habla en el idioma del juego. Las palabras propias del mod están verificadas por oído solo en español; en los otros idiomas están traducidas sin que un hablante las haya revisado. Si una palabra está mal, es un error que vale la pena reportar.

## Notas

- El mod no modifica ningún archivo del juego.
- UE4SS es del equipo RE-UE4SS, bajo licencia MIT; `prism.dll` y `tolk.dll` son de [PRISM](https://github.com/ethindp/prism), bajo MPL 2.0. Ver `THIRD-PARTY.md`.
- Para desinstalar, borrá `dwmapi.dll` y la carpeta `ue4ss`.
- El código fuente del mod todavía no es público; lo será cuando el mod se asiente con el uso. La descarga es libre de usar.
