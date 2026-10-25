# Sygmatch Downloader

**Descarga videos y audio de internet con unos pocos clics.** Pegas el enlace, eliges la calidad y el formato, y el programa se encarga del resto: descarga, convierte, comprueba el resultado y te avisa cuando termina.

<img width="1362" height="729" alt="image" src="https://github.com/user-attachments/assets/28def553-a8f9-43cd-814f-287f471548e5" />


**Contenido:**
[Para qué sirve](#para-qué-sirve) ·
[Requisitos](#requisitos) ·
[Cómo empezar](#cómo-empezar) ·
[La pantalla](#la-pantalla) ·
[Todas las opciones](#todas-las-opciones) ·
[Botones](#los-botones) ·
[Progreso y registro](#progreso-y-registro) ·
[Avisos del programa](#avisos-que-puede-mostrar-el-programa) ·
[Actualizaciones](#actualizaciones-automáticas) ·
[Prueba y licencia](#prueba-gratuita-y-licencia) ·
[Preguntas frecuentes](#preguntas-frecuentes)

---

## Para qué sirve

- Guardar un **video** en tu equipo para verlo sin conexión (en MP4 o MKV).
- Guardar solo el **audio** de un video, en el formato que prefieras (MP3, M4A, FLAC, OPUS o WAV).
- Descargar **listas de reproducción completas**, o solo una parte.
- Descargar **varios enlaces seguidos**: los pones uno debajo de otro y el programa los procesa en orden.
- Descargar contenido que **exige iniciar sesión**, usando las cookies de tu navegador o de un archivo.

Funciona con YouTube y con muchísimos otros sitios de video y audio.

---

## Requisitos

| Requisito | Detalle |
|---|---|
| Sistema | Windows 10 u 11 de 64 bits |
| Internet | Para descargar y, la primera vez, para instalar las herramientas |
| Espacio | Las herramientas ocupan varios cientos de MB, más lo que pesen tus descargas |
| Instalación | **Ninguna.** No se instala: se abre y se usa |

---

## Cómo empezar

1. **Abre el programa** (`Sygmatch Downloader.exe`). Arranca con la ventana **maximizada**.
2. **La primera vez** descarga e instala solo las herramientas que necesita (yt-dlp, ffmpeg y Deno). Verás una barra de progreso; puede tardar unos minutos según tu internet. Las siguientes veces abre mucho más rápido.
3. **Pega tu enlace** en el cuadro grande de la izquierda.
4. **Elige** el tipo de contenido y la calidad.
5. Pulsa **Iniciar descarga**. Al terminar suena un aviso y el archivo está en tu carpeta de destino.

> Si prefieres usar el archivo `.ps1` en lugar del `.exe`: clic derecho sobre `Sygmatch Downloader.ps1` → **Ejecutar con PowerShell**.

---

## La pantalla

```
┌──────────────────────────────────────────────────────────────────────┐
│ SYGMATCH            ● Estado de licencia   [Licencia]   [☀ / 🌙]    │  ← cabecera
├───────────────────────────┬──────────────────────────────────────────┤
│  OPCIONES (izquierda)     │  PROGRESO Y REGISTRO (derecha)           │
│  Enlaces                  │  Barra de progreso, velocidad, tiempo    │
│  Contenido · Alcance      │  Barra de la cola                        │
│  Calidad / formato        │  Registro de lo que ocurre               │
│  Rango · Cookies · Perfil │  [Abrir carpeta] [Copiar] [Limpiar]      │
│  Argumentos extra         │  Versiones · [Actualizar herramientas]   │
│  Carpeta · casillas       │                                          │
│  [Iniciar] [Cancelar]     │                                          │
└───────────────────────────┴──────────────────────────────────────────┘
```

Si tu pantalla es pequeña, el panel de opciones tiene una barra de desplazamiento.

---

## Todas las opciones

### Enlaces (uno por línea)
Aquí pegas los enlaces de lo que quieres descargar, **uno por línea**.

- Al pegar un enlace (con `Ctrl+V`, clic derecho → Pegar o el botón **Pegar**), el cursor salta solo a la línea siguiente, para que pegues el próximo sin que se amontonen.
- Si pegas varios enlaces a la vez, cada uno queda en su propia línea.
- Las líneas que no sean un enlace válido se ignoran (el programa te avisa en el registro).
- Si algún enlace **falla**, se queda en la lista para que puedas reintentarlo. Los que se descargaron bien desaparecen.

### Contenido
- **Video (MP4 / MKV):** descarga imagen y sonido juntos.
- **Solo audio (MP3, FLAC, M4A…):** descarga únicamente el sonido.

### Alcance
- **Solo este enlace:** descarga únicamente el video del enlace, aunque pertenezca a una lista.
- **Lista completa:** descarga todos los videos de la lista de reproducción. Se crea una carpeta con el nombre de la lista y los archivos quedan numerados (`001 - título`, `002 - título`…). Entre un video y otro el programa espera unos segundos para no saturar al sitio.

### Rango de lista (ej: 1-5, 8)
Solo se activa con **Lista completa**. Sirve para descargar una parte de la lista.
Ejemplos: `1-5` (del primero al quinto) · `1-3, 8` (los tres primeros y el octavo). Vacío = toda la lista.

### Calidad / formato y conversión

**Si elegiste Video:**

| Opción | Qué significa |
|---|---|
| Mejor calidad disponible (MP4 o MKV) | La más alta que ofrezca el sitio (puede llegar a 4K u 8K). Se guarda en MP4 o, si no es posible, en MKV |
| 2160p · 4K (MP4 o MKV) | Como máximo 4K |
| 1440p · 2K (MP4 o MKV) | Como máximo 2K |
| **1080p Full HD · MP4 compatible** | **Recomendada.** Se ve bien en casi cualquier reproductor, televisor o celular |
| 720p HD · MP4 compatible | Más liviano, calidad HD |
| 480p · MP4 compatible | Archivos pequeños |
| 360p · MP4 compatible | Los más livianos |

*"MP4 compatible" significa que el programa prefiere el códec H.264 + AAC, el que reproduce prácticamente todo. En resoluciones muy altas (4K) algunos sitios no ofrecen ese códec.*

**Si elegiste Solo audio:**

| Opción | Qué significa |
|---|---|
| MP3 · 320 kbps (máxima calidad) | El formato más universal, en su mejor calidad |
| MP3 · 192 kbps | Buena calidad con menos peso |
| MP3 · 128 kbps | El más liviano |
| M4A (AAC) · 256 kbps | Buena calidad con poco peso; ideal para el ecosistema Apple |
| FLAC · sin pérdida | Formato sin compresión con pérdida; ocupa más espacio |
| OPUS · 160 kbps | Muy buena calidad con archivos pequeños |
| WAV · sin comprimir | Audio crudo, archivos muy grandes; para edición |
| Original (sin conversión) | El audio tal como lo publica el sitio, sin convertirlo |

> **Dato importante:** si el audio original ya tiene pérdida (como el de YouTube), convertirlo a FLAC o WAV **no mejora su calidad**; solo cambia el formato del archivo.

**La conversión se comprueba.** Al terminar cada descarga, el programa verifica que el archivo realmente quedó en el formato que pediste. Si no fue así, lo convierte con ffmpeg. En el registro verás una línea como `Verificado · FLAC · 44.1 kHz · 4.2 MB` que te lo confirma.

### Cookies del navegador
Sirven para dos casos: contenido que **solo se ve con tu cuenta iniciada** (restricción de edad, contenido para miembros…) y sitios que a veces piden comprobar que no eres un robot. Tienes tres formas de usarlas:

| Opción | Cuándo usarla |
|---|---|
| **No usar** | Lo normal. Déjalo así si no lo necesitas |
| **Chrome, Edge, Firefox, Brave, Opera o Vivaldi** | El programa toma las cookies de ese navegador. Debes tener la sesión iniciada allí |
| **Archivo cookies.txt…** | Eliges un archivo de cookies exportado desde tu navegador (formato Netscape). Es la opción más fiable cuando el navegador falla |

**Consejos:**
- **Firefox o un archivo cookies.txt son las opciones más fiables.** Chrome, Edge y Brave cifran sus cookies y las bloquean mientras están abiertos; en muchos equipos fallan incluso cerrándolos.
- Para crear un `cookies.txt`, usa una extensión de tu navegador que exporte cookies en formato Netscape (usa solo extensiones de confianza).
- **Las cookies son datos sensibles de tu cuenta.** No compartas ese archivo con nadie.
- Al elegir "Archivo cookies.txt…" se abre una ventana para seleccionarlo; el programa recuerda cuál elegiste. Si el archivo ya no existe, descarga sin cookies y te avisa.

### Botón Perfil
Solo se activa cuando has elegido un navegador. Si ese navegador tiene **varios perfiles** (por ejemplo, uno personal y uno de trabajo), te deja elegir de cuál tomar las cookies.

- Funciona con Chrome, Edge, Firefox, Brave y Vivaldi. Con Opera se usa el perfil por defecto.
- Al elegir un navegador con varios perfiles, la ventana de selección se abre sola.
- Si solo hay un perfil, se usa ese sin preguntar.
- Cuando eliges uno, la etiqueta de la lista cambia a `Cookies · nombre del perfil`.

### Argumentos extra de yt-dlp (avanzado, opcional)
Un cuadro de texto para **usuarios avanzados**. El programa descarga gracias a una herramienta llamada **yt-dlp**, que tiene cientos de opciones. Este cuadro te permite añadirle órdenes propias que el programa no ofrece en pantalla. **Si no sabes qué escribir, déjalo vacío: el programa funciona perfectamente sin él.**

**Cómo se usa:** escribe las opciones separadas por espacios. Si un valor lleva espacios, ponlo entre comillas. El programa las añade al final de la orden de descarga, y se recuerdan para la próxima vez.

| Ejemplo | Qué hace |
|---|---|
| `--limit-rate 2M` | Limita la velocidad de descarga a 2 MB por segundo |
| `--retries 20` | Reintenta más veces ante cortes de conexión |
| `--proxy http://127.0.0.1:8080` | Descarga a través de un proxy |
| `--embed-chapters` | Guarda los capítulos del video dentro del archivo |
| `--write-description` | Guarda la descripción del video en un archivo de texto |
| `--remote-components ejs:github` | Sugerido por el programa si falla el "desafío JavaScript" de YouTube |

**Precauciones:**
- **No uses** opciones que el programa ya maneja por su cuenta (`-o`, `-P`, `--progress-template`, `--print-to-file`, `--newline`, `--ffmpeg-location`): romperían la barra de progreso o el guardado.
- Como se añaden al final, **pueden anular** lo que elegiste arriba (por ejemplo, `-f` cambiaría la calidad).
- **Evita `--exec`**: ejecuta programas de tu equipo después de cada descarga.
- Si escribes una opción que no existe, yt-dlp la rechaza y **todas las descargas fallan**. Si eso pasa justo después de usar este cuadro, vacíalo, o activa **Mostrar registro detallado** para ver el motivo.

Puedes consultar todas las opciones disponibles en la [documentación de yt-dlp](https://github.com/yt-dlp/yt-dlp#usage-and-options).

### Carpeta de destino
Es donde se guardan tus descargas. Pulsa **Examinar** para elegirla con el selector de carpetas de Windows (con barra de direcciones, panel lateral y botón "Nueva carpeta"). Por defecto es `Descargas\Sygmatch`. El programa recuerda tu elección.

### Casillas de opciones

| Casilla | Para qué sirve |
|---|---|
| **Incrustar metadatos y carátula** | Guarda dentro del archivo el título, el artista y la imagen de portada, para que tu reproductor los muestre. La carátula se incrusta en MP3, M4A, FLAC, OPUS y en video; no en WAV ni en audio "Original" |
| **Incrustar subtítulos (español / inglés)** | Agrega al video los subtítulos en español e inglés, incluidos los generados automáticamente, cuando existan. Solo funciona con **Video** |
| **Omitir elementos ya descargados** | Mantiene un historial para no volver a bajar lo mismo. Útil con listas que vas actualizando |
| **Mostrar registro detallado** | Muestra en el registro todos los mensajes técnicos. Normalmente no hace falta; sirve para investigar un problema |
| **Buscar actualizaciones de herramientas al iniciar** | Revisa si hay versiones nuevas de yt-dlp, ffmpeg y Deno (como máximo una vez cada 24 horas) |

---

## Los botones

| Botón | Qué hace |
|---|---|
| **Iniciar descarga** | Empieza a procesar todos los enlaces de la lista, uno tras otro |
| **Cancelar** | Detiene la descarga en curso al instante. Los enlaces pendientes se quedan en la lista |
| **Pegar** | Pega lo que hayas copiado, con cada enlace en su propia línea |
| **Perfil** | Elige el perfil del navegador del que tomar las cookies |
| **Examinar** | Elige la carpeta de destino |
| **Abrir carpeta** | Abre la carpeta de destino en el Explorador |
| **Copiar registro** | Copia todo el texto del registro (útil para pedir ayuda) |
| **Limpiar** | Borra el registro de la pantalla |
| **Actualizar herramientas** | Busca e instala ahora las versiones más recientes de yt-dlp, ffmpeg y Deno |
| **Licencia / Activar licencia** | Abre la ventana para ver tu estado y activar tu clave |
| **☀ / 🌙 (interruptor)** | Cambia entre modo claro (sol) y modo oscuro (luna). El programa recuerda tu elección |

---

## Progreso y registro

- **La barra grande** muestra el avance de lo que se descarga, con porcentaje.
- **Debajo de la barra** ves cuánto se lleva descargado, la velocidad y cuánto tiempo falta.
- **La barra delgada** muestra el avance de toda la cola ("enlace 2 de 5").
- Cuando el programa une video y audio o convierte el formato, la barra se anima y dice qué hace (*Convirtiendo audio…*, *Uniendo video y audio…*). Es normal que entonces el porcentaje no avance.
- **El registro** cuenta lo importante: qué archivo se descarga, si se convirtió, avisos, errores y dónde quedó guardado.
- Abajo a la derecha verás las versiones instaladas de yt-dlp, ffmpeg y Deno.

### La ventana siempre responde
Las descargas, conversiones y actualizaciones se ejecutan **en segundo plano**. Puedes minimizar, maximizar, mover o redimensionar la ventana en cualquier momento, incluso con una descarga en curso.

---

## Avisos que puede mostrar el programa

El programa intenta explicarte los problemas en lenguaje claro:

| Aviso | Qué significa y qué hacer |
|---|---|
| *No se pudieron leer las cookies del navegador* | Chrome, Edge o Brave bloquean sus cookies. Usa **Firefox** (con sesión iniciada) o **Archivo cookies.txt…** |
| *Aviso: el navegador está abierto y bloquea su base de cookies* | Si la descarga falla, cierra ese navegador o cambia a Firefox / cookies.txt |
| *YouTube bloqueó temporalmente tu conexión (429 / anti-bot)* | Espera 30-60 minutos sin descargar, usa cookies de una sesión iniciada, cambia de red o desactiva la VPN. Actualizar las herramientas no lo soluciona |
| *Falla el desafío JavaScript de YouTube* | Pulsa **Actualizar herramientas**. Si persiste, prueba el argumento extra `--remote-components ejs:github` |
| *Pediste 1080p pero el archivo es de 480p* | El video quizá no ofrece más calidad, o YouTube limitó los formatos (suele pasar sin cookies de una sesión iniciada) |
| *El archivo no quedó en MP3 / FLAC…; se convertirá con ffmpeg* | Es la comprobación automática del formato; el programa lo corrige solo |
| *No se descargó nada nuevo (¿ya estaba descargado?)* | Con **Omitir elementos ya descargados** activado, ese contenido ya estaba en el historial |

---

## Actualizaciones automáticas

Los sitios web cambian a menudo, y las herramientas que usa el programa se actualizan para seguirles el ritmo. Por eso Sygmatch Downloader:

- Revisa **una vez al día**, al abrirse, si hay versiones nuevas de yt-dlp, ffmpeg y Deno (puedes desactivarlo en su casilla).
- Descarga las nuevas versiones, **comprueba que no estén dañadas** y solo entonces reemplaza las anteriores. Si algo sale mal, conserva la versión que ya funcionaba.
- Si una descarga falla porque el sitio cambió, **se actualiza y reintenta una vez** automáticamente.
- Puedes forzarlo cuando quieras con **Actualizar herramientas**.

---

## Prueba gratuita y licencia

**Tienes 7 días de prueba con todas las funciones**, desde la primera vez que abres el programa. Arriba a la derecha ves cuántos días te quedan.

Cuando termina la prueba, para seguir descargando necesitas una **licencia**, que:
- Es **para un solo equipo** (queda vinculada a tu computadora).
- **Funciona sin conexión** una vez activada.
- Se activa en menos de un minuto.

### Cómo activarla
1. Pulsa **Activar licencia** (arriba a la derecha).
2. Pulsa **Copiar** junto a *ID de tu equipo*.
3. Envía ese ID por correo o WhatsApp (datos abajo) y recibirás tu clave.
4. Pega la clave en el cuadro y pulsa **Activar licencia**.

### Sobre el valor de la licencia
El valor es significativo: refleja las horas de trabajo y el esfuerzo detrás de este programa. **Tú, como usuario, le pones el precio a ese trabajo:** escríbenos y acordamos un aporte que consideres justo.

📧 **Correo:** sygmatch@gmail.com
💬 **WhatsApp:** +593 98 712 0183

---

## Dónde guarda sus cosas

| Qué | Dónde |
|---|---|
| Tus descargas | La carpeta que elijas (por defecto `Descargas\Sygmatch`) |
| Las herramientas | Carpeta `tools`, junto al programa (o en `%LOCALAPPDATA%\Sygmatch\Downloader\tools` si esa carpeta no permite escribir) |
| Tus ajustes y el historial | `%LOCALAPPDATA%\Sygmatch\Downloader` |
| Registro de errores | `%LOCALAPPDATA%\Sygmatch\Downloader\error.log` |

---

## Preguntas frecuentes

**Windows o mi antivirus dice que el programa es sospechoso.**
Es común en programas creados con PowerShell y convertidos a `.exe`. Si lo descargaste de este repositorio, puedes agregarlo como excepción.

**Al abrirlo por primera vez tarda en iniciar.**
Es normal: el programa prepara su interfaz y descarga sus herramientas.

**Dice "Faltan herramientas".**
Comprueba tu conexión a internet y pulsa **Actualizar herramientas**.

**Una descarga falló.**
Ese enlace se queda en la lista. Pulsa **Iniciar descarga** de nuevo. Si sigue fallando, activa **Mostrar registro detallado**, reintenta y mira el mensaje; también puedes usar **Copiar registro** y enviárnoslo.

**YouTube me pide "confirmar que no eres un robot" o me da error 429.**
Mira la tabla de [avisos](#avisos-que-puede-mostrar-el-programa): lo más eficaz suele ser usar cookies de una sesión iniciada (Firefox o cookies.txt) y esperar un rato.

**Descargué en 1080p y el video salió peor.**
Lee el aviso "Pediste Xp pero el archivo es de Yp" en el registro. Suele ocurrir cuando el video no ofrece esa calidad o cuando no se usan cookies de una sesión iniciada.

**Pegué mi clave y no se activa.**
Revisa que esté completa y que se generó con el ID que muestra **tu** programa (el ID cambia entre equipos). Si no puedes resolverlo, escríbenos.

**¿Puedo usar mi licencia en otra computadora?**
La licencia está ligada a un equipo. Si cambias de computadora, escríbenos.

---

## Uso responsable

Usa este programa solo con contenido que tengas derecho a descargar: tuyo, de dominio público, con licencia que lo permita, o para uso personal donde la ley de tu país lo autorice. Respetar los derechos de autor y las condiciones de cada sitio es **responsabilidad de quien lo usa**. Este proyecto no está afiliado a YouTube ni a ningún otro sitio.

---

<details>
<summary><b>Para desarrolladores: compilar a .exe</b></summary>

Requiere el módulo [PS2EXE](https://github.com/MScholtes/PS2EXE):

```powershell
Install-Module ps2exe -Scope CurrentUser
Invoke-ps2exe ".\Sygmatch Downloader.ps1" ".\Sygmatch Downloader.exe" `
    -noConsole -noOutput -noError -STA -DPIAware -x64 `
    -title "Sygmatch Downloader" -company "Sygmatch" -version 2.0.3.0
```

`-STA` es obligatorio para que funcione la interfaz. Puedes añadir `-iconFile` con tu icono y `-requireAdmin` si quieres que pida permisos de administrador (no es necesario para el funcionamiento normal).

Antes de compilar, pega tu **clave pública** de licencias en la línea `$script:LicensePublicKeyB64` del script.

</details>

---

**Sygmatch Downloader** · hecho por [Sygmatch](https://github.com/Sygmatch)
