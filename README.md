# Radiohomeless.org - Web Player

Interfaz web y sistema de reproducción en tiempo real para **Radio Homeless**, una estación de radio por internet y proyecto alternativo de contracultura dedicado a la música independiente, fanzines y contenido sonoro experimental.

## Objetivo del Proyecto

Proporcionar una experiencia de escucha web ligera, estable y estéticamente coherente con la identidad DIY/brutalista de la radio, priorizando el rendimiento, la accesibilidad y la reactividad visual sin depender de frameworks pesados.

## Características Principales

- **Reproducción de Stream en Vivo:** Conexión directa a servidores Icecast/Shoutcast con manejo robusto de reconexión automática ante caídas de red.
- **Visualización de Audio en Tiempo Real:** Medidor ASCII reactivo impulsado por la **Web Audio API** (`AnalyserNode`), calculando RMS en tiempo real sin sobrecargar la CPU.
- **Metadata en Vivo:** Polling automático cada 5 segundos para mostrar la canción actual (`now-playing`) y el historial de las últimas 5 transmisiones.
- **UX Mejorada:** Estados visuales claros (play/pause/stop) con retroalimentación inmediata, manteniendo la estética minimalista original.
- **Zero Dependencies:** 100% Vanilla JavaScript, HTML5 y CSS3. Sin jQuery, React ni librerías de terceros innecesarias.

## Stack Tecnológico

- **Frontend:** HTML5, CSS3 (Custom Properties, Flexbox), Vanilla JavaScript (ES6+).
- **Audio:** Web Audio API (`AudioContext`, `AnalyserNode`, `MediaElementSource`).
- **Backend/API:** Fetch API para consultas a `/config` y `/api/now-playing`.

### Cómo ejecutar localmente

Dado que la Web Audio API requiere un contexto seguro o un servidor local para evitar problemas de CORS y autoplay:

Clona el repositorio:

```
git clone https://github.com/tu-usuario/radiohomeless.org.git
cd radiohomeless.org
```

### Estructura de Archivos

```
/
├── index.html          # Estructura semántica principal
├── static/
│   ├── radio.css       # Estilos base (tipografía, layout, variables)
│   ├── radio.js        # Lógica principal del reproductor y Web Audio API
│   └── ...             # Assets (imágenes, animaciones)
└── README.md
```
