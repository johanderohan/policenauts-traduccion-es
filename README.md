# Policenauts — Traducción al castellano

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Traducción al **español de España** de *Policenauts* para PlayStation japonesa
(Konami, 1996): los **dos discos de la aventura** y el disco de extras
**Private Collection**. Voces japonesas originales con subtítulos en castellano.

La traducción se reparte como **tres parches XDELTA**, uno por disco. No incluye
el juego: necesitas tu propia copia japonesa.

## Estado

Última versión: **[v1.0](../../releases/tag/v1.0)**.

| Parte | Estado |
|---|---|
| Guion de la aventura | 27 bancos, 16.158 registros traducidos y con segunda lectura |
| Subtítulos de voz | 5.402 subtítulos en 1.007 clips (discos 1 y 2) |
| Vídeos | 526 subtítulos en 39 películas, incluido el prólogo |
| Menús, nombres y avisos | Menús, placas de nombre, tarjeta de memoria, cambio de disco y persecución |
| Private Collection | Enciclopedia (198 fichas), entrevistas, making, créditos, fichas de actores, modo de disparos y más de 600 rótulos gráficos |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿**, en las fuentes Gothic y Mincho |

Se conservan los logotipos (POLICENAUTS, KONAMI), los rótulos en inglés del
original («ACT», «NOW LOADING», «WARNING») y el contraste de las fuentes originales.

**Se queda en japonés**, porque no cabe en el disco con garantías: el texto
grabado dentro de los vídeos, los storyboards y notas manuscritas de las láminas
de producción, el guion del making (visor vertical) y unos pocos rótulos gráficos.

### Comprobaciones

Probado en emulador (Mednafen PSX): arranque, título, cambio de fuente, prólogo
con subtítulos en ambas fuentes, primeros diálogos, guardado y carga, cambio de
disco 1→2 y 2→1, los 27 bancos de guion cargados en castellano, 51 clips de voz,
nueve vídeos, la persecución, avisos de tarjeta y el capítulo final. En Private
Collection: menús, enciclopedia con enlaces, cronología, entrevistas, making,
créditos, actores y modo de disparos.

Cada parche se ha reaplicado sobre el BIN original y el resultado coincide byte
a byte con la imagen probada.

**Limitaciones:** la revisión de textos se ha hecho con asistencia de IA, no por
revisores humanos independientes. No se ha jugado una partida completa de principio
a fin, ni se ha probado en consola real. Algunas escenas se comprobaron
cargándolas directamente. Si encuentras un error, abre una incidencia con una captura.

## Cómo aplicar los parches

1. Descarga los tres `.xdelta` de **[Releases](../../releases)**.
2. Comprueba que tus BIN japoneses son exactamente estos:

   | Disco | Serie | Tamaño | MD5 |
   |---|---|---:|---|
   | Disco 1 | SLPS-00215 | 747.752.544 | `fea7dc633f420a1f5fea8e3e632d6a92` |
   | Disco 2 | SLPS-00216 | 612.905.328 | `387c3719260194e4e6c975c0614b0dec` |
   | Private Collection | SLPS-00228 | 597.687.888 | `e231ba723a8738ac473827e9789ba76a` |

3. Aplica cada parche a su disco:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "original.bin" parche.xdelta "traducido.bin"`
4. Comprueba los resultados:

   | Disco | Tamaño | MD5 |
   |---|---:|---|
   | Disco 1 | 759.103.296 | `e469500fb70de336767c72b48e95b2e4` |
   | Disco 2 | 759.103.296 | `1a0bb9e89ec7a19bd892baad5e7f7282` |
   | Private Collection | 613.864.944 | `e0f8de0d9d725053be53027c6319b347` |

5. Edita cada `.cue` para que apunte al nuevo `.bin`. Para cambiar de disco en el
   emulador, lo más cómodo es una lista `.m3u` con los dos `.cue` de la aventura.
6. Empieza una partida nueva. No se ha probado a cargar partidas guardadas con
   la versión japonesa.

## Créditos y aviso

Traducción de aficionados sin relación con Konami. Solo se distribuyen parches
para modificar una copia propia; no se incluyen imágenes de disco, BIOS ni
archivos del juego. Auxiliares de sectores EDC/ECC basados en
[TheAti1/policenauts-disc1-translation-tools](https://github.com/TheAti1/policenauts-disc1-translation-tools) (MIT).
