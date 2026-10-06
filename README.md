# Sygmatch Downloader

**Descarga videos y audio de internet con unos pocos clics.** Pegas el enlace, eliges la calidad y el formato, y el programa hace el resto: descarga, convierte y te avisa cuando termina.

<!-- Sugerencia: agrega aquí una captura de pantalla del programa, por ejemplo:
![Sygmatch Downloader](capturas/principal.png) -->

---<img width="1363" height="722" alt="image" src="https://github.com/user-attachments/assets/35a9968c-d2ef-45e5-a2bb-57c00b45cebb" />


## ¿Para qué sirve?

- Guardar un **video** en tu equipo para verlo sin conexión (en MP4 o MKV).
- Guardar solo el **audio** de un video, en el formato que prefieras (MP3, FLAC, M4A, OPUS, WAV).
- Descargar **listas de reproducción completas**, o solo una parte de ellas.
- Descargar **varios enlaces a la vez**: los pones uno debajo de otro y el programa los procesa en orden.

Funciona con YouTube y con muchísimos otros sitios de video y audio.

---

## Qué necesitas

| Requisito | Detalle |
|---|---|
| Sistema | Windows 10 u 11 de 64 bits |
| Internet | Para descargar, y la primera vez para instalar las herramientas |
| Espacio | Unos 300 MB libres para las herramientas, más lo que ocupen tus descargas |
| Instalación | **Ninguna.** No se instala; se abre y se usa |

---

## Cómo empezar

1. **Abre el programa** (`Sygmatch Downloader.exe`).
2. **La primera vez** descargará e instalará solo las herramientas que necesita (yt-dlp, ffmpeg y Deno). Verás una barra de progreso; puede tardar unos minutos según tu internet. Las siguientes veces abre al instante.
3. **Pega tu enlace** en el cuadro grande de la izquierda.
4. **Elige** el tipo de contenido y la calidad.
5. Pulsa **Iniciar descarga** y espera. Cuando termine, suena un aviso y el archivo está en tu carpeta de destino.



## Las opciones, una por una

### Enlaces
Aquí pegas los enlaces de lo que quieres descargar. **Uno por línea.**

- Al pegar un enlace (con `Ctrl+V`, clic derecho → Pegar o el botón **Pegar**), el cursor salta solo a la línea siguiente, para que pegues el próximo sin que se amontonen.
- Si algún enlace falla, **se queda en la lista** para que puedas reintentarlo. Los que se descargaron bien desaparecen.

### Contenido
- **Video (MP4 / MKV):** descarga imagen y sonido juntos.
- **Solo audio (MP3, FLAC, M4A…):** descarga únicamente el sonido.

### Alcance
- **Solo este enlace:** descarga únicamente el video del enlace, aunque pertenezca a una lista.
- **Lista completa:** descarga todos los videos de la lista de reproducción. Se crea una carpeta con el nombre de la lista y los archivos quedan numerados (`001 - título`, `002 - título`…).

### Rango de lista
Solo se activa con **Lista completa**. Sirve para descargar una parte de la lista.
Ejemplos: `1-5` (del primero al quinto) · `1-3, 8` (los tres primeros y el octavo). Si lo dejas vacío, se descarga toda la lista.

### Calidad / formato y conversión

**Si elegiste Video:**

| Opción | Qué significa |
|---|---|
| Mejor calidad disponible | La más alta que ofrezca el sitio (puede llegar a 4K u 8K). Se guarda en MP4 o, si no es posible, MKV |
| 2160p · 4K / 1440p · 2K | Calidad alta, con ese tope de resolución |
| 1080p Full HD · MP4 compatible | **Recomendada.** Se ve bien en casi cualquier reproductor, televisor o celular |
| 720p HD / 480p / 360p · MP4 compatible | Archivos más livianos. Útiles si tienes poco espacio o internet lenta |

*"MP4 compatible" significa que el programa prefiere el códec H.264 + AAC, el que reproduce prácticamente todo. En resoluciones muy altas (4K) algunos sitios no ofrecen ese códec.*

**Si elegiste Solo audio:**

| Opción | Qué significa |
|---|---|
| MP3 · 320 / 192 / 128 kbps | El formato más universal. 320 es la mejor calidad; 128 pesa menos |
| M4A (AAC) · 256 kbps | Buena calidad con poco peso; ideal para iPhone y Apple Music |
| FLAC · sin pérdida | Formato sin compresión con pérdida. Ocupa más espacio |
| OPUS · 160 kbps | Muy buena calidad con archivos pequeños |
| WAV · sin comprimir | Audio crudo, archivos muy grandes. Para edición profesional |
| Original (sin conversión) | Te da el audio tal como lo publica el sitio, sin convertirlo |

> **Dato importante:** si el audio original ya tiene pérdida (como el de YouTube), convertirlo a FLAC o WAV **no mejora su calidad**; solo cambia el formato del archivo.

**La conversión es verificada.** Al terminar cada descarga el programa comprueba que el archivo realmente quedó en el formato que pediste. Si no fue así, lo convierte automáticamente. En el registro verás una línea como `Verificado · FLAC · 44.1 kHz · 4.2 MB` que te lo confirma.

### Cookies del navegador
Para contenido que **solo se ve con tu cuenta iniciada** (por ejemplo, con restricción de edad). Elige el navegador donde tienes la sesión abierta: Chrome, Edge, Firefox, Brave, Opera o Vivaldi. Si no lo necesitas, déjalo en **No usar**.
*Nota: con algunos navegadores (a veces Chrome) puede no funcionar; prueba con Edge o Firefox.*

### Carpeta de destino
Es donde se guardan tus descargas. Pulsa **Examinar** para elegirla con el explorador de Windows. Por defecto es `Descargas\Sygmatch`. El programa recuerda tu elección.

### Casillas de opciones

| Casilla | Para qué sirve |
|---|---|
| **Incrustar metadatos y carátula** | Guarda dentro del archivo el título, el artista y la imagen de portada, para que tu reproductor los muestre |
| **Incrustar subtítulos (español / inglés)** | Agrega los subtítulos al video, si existen. Solo funciona con **Video** |
| **Omitir elementos ya descargados** | Mantiene un historial para no volver a bajar lo mismo. Útil con listas que vas actualizando |
| **Mostrar registro detallado** | Muestra en el registro todos los mensajes técnicos. Normalmente no hace falta; sirve para investigar un problema |
| **Buscar actualizaciones de herramientas al iniciar** | Revisa si hay versiones nuevas de yt-dlp, ffmpeg y Deno (máximo una vez cada 24 horas) |

---

## Los botones

| Botón | Qué hace |
|---|---|
| **Iniciar descarga** | Empieza a procesar todos los enlaces de la lista, uno tras otro |
| **Cancelar** | Detiene la descarga en curso. Los enlaces pendientes se quedan en la lista |
| **Pegar** | Pega lo que hayas copiado, con cada enlace en su propia línea |
| **Examinar** | Elige la carpeta de destino |
| **Abrir carpeta** | Abre la carpeta de destino en el Explorador |
| **Copiar registro** | Copia todo el texto del registro (útil para pedir ayuda) |
| **Limpiar** | Borra el registro de la pantalla |
| **Actualizar herramientas** | Busca e instala ahora las versiones más recientes de yt-dlp, ffmpeg y Deno |
| **Licencia / Activar licencia** | Abre la ventana para ver tu estado y activar tu clave |
| **☀ / 🌙 (interruptor)** | Cambia entre modo claro (sol) y modo oscuro (luna). El programa recuerda tu elección |

---

## Cómo leer la pantalla de progreso

- **La barra grande** muestra el avance de lo que se está descargando, con porcentaje.
- **Debajo de la barra** ves cuánto se lleva descargado, la velocidad y cuánto tiempo falta.
- **La barra delgada de abajo** muestra el avance de toda la cola ("enlace 2 de 5").
- Cuando el programa une el video con el audio o convierte el formato, la barra se anima y dice qué está haciendo (*Convirtiendo audio…*, *Uniendo video y audio…*). Es normal que en ese momento el porcentaje no avance.
- **El registro** (la zona de texto) cuenta lo importante: qué archivo se descarga, si se convirtió, si hubo avisos o errores y dónde quedó guardado.

---

## Actualizaciones automáticas

Los sitios web cambian a menudo, y las herramientas que usa el programa se actualizan para seguirles el ritmo. Por eso Sygmatch Downloader:

- Revisa **una vez al día**, al abrirse, si hay versiones nuevas (puedes desactivarlo en la casilla correspondiente).
- Descarga las nuevas versiones, **comprueba que no estén dañadas** y solo entonces reemplaza las anteriores. Si algo sale mal, conserva la versión que ya funcionaba.
- Si una descarga falla porque el sitio cambió, **se actualiza y reintenta una vez** automáticamente.
- También puedes forzarlo cuando quieras con el botón **Actualizar herramientas**.

---

## Prueba gratuita y licencia

**Tienes 7 días de prueba con todas las funciones**, desde la primera vez que abres el programa. En la parte superior derecha ves cuántos días te quedan.

Cuando termina la prueba, para seguir descargando necesitas una **licencia**. La licencia:

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
Es común en programas `.exe`. Si lo descargaste de este repositorio, puedes agregarlo como excepción.

**Al abrirlo por primera vez tarda en iniciar.**
Es normal: el programa prepara su interfaz y, si hace falta, descarga sus herramientas.

**Dice "Faltan herramientas".**
Comprueba tu conexión a internet y pulsa **Actualizar herramientas**.

**Una descarga falló.**
Ese enlace se queda en la lista. Pulsa **Iniciar descarga** de nuevo; si sigue fallando, prueba **Actualizar herramientas** y reintenta. Si el problema continúa, usa **Copiar registro** y envíanoslo.

**Pegué mi clave y no se activa.**
Revisa que la clave esté completa y que se haya generado con el ID que muestra **tu** programa (el ID cambia entre equipos). Si no puedes resolverlo, escríbenos.

**¿Puedo usar mi licencia en otra computadora?**
La licencia está ligada a un equipo. Si cambias de computadora, escríbenos.

---

## Uso responsable

Usa este programa solo con contenido que tengas derecho a descargar: tuyo, de dominio público, con licencia que lo permita, o para uso personal donde la ley de tu país lo autorice. Respetar los derechos de autor y las condiciones de cada sitio es **responsabilidad de quien lo usa**. Este proyecto no está afiliado a YouTube ni a ningún otro sitio.
