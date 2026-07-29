# Oco AI · Demos de agentes

Demos en vivo de agentes de IA por industria de **Oco AI** (Omega AI Consulting).
Publicado con GitHub Pages: https://abelzapatav.github.io/oco-ai-demos/

Sitio estático (HTML + CSS + JS, sin build). Cada demo es un chat conectado a un
webhook de n8n; el hub (`index.html`) enlaza a los 4 agentes.

## Estructura

```
oco-ai-demos/
├── index.html               # hub (landing de demos)
├── demo-ecommerce/          # Asistente de Tienda
├── demo-inmobiliaria/       # Agente Inmobiliario
├── demo-ventacarnes/        # Asesor de Carnes
├── demo-salon.spa/          # Asistente de Belleza
└── assets/
    ├── demo.css             # estilos compartidos de las páginas de chat
    ├── logo/                # wordmark + monograma oficiales
    ├── favicon-512.png · apple-touch-icon.png
    └── og-cover.jpg         # imagen social
```

## Marca

Alineado con la web principal (omegaconsultingai.com): aurora esmeralda
(`#071310` / acento `#2DCA8C`), tipografía **Sora + DM Sans**, logo oficial,
iconos SVG. Un cambio de estilo de las demos se hace en `assets/demo.css`.

## ⚠️ Importante para editar una demo

Cada demo tiene su lógica de chat en el bloque `<script>` al final del archivo,
que empieza en `const WEBHOOK_URL`. **No modificar ese bloque** salvo el
`WEBHOOK_URL` y la clave de sesión (`*_sid`) — es lo único que cambia entre
demos. El resto del script es idéntico en las 4.
