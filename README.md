# MALITOX CODE — Web v1

Web negra y morada inspirada en la distribución de una aplicación de programación con IA: barra lateral, sesiones, chat, editor y descarga de código. Es un diseño original.

## Publicar en GitHub Pages

1. Crea un repositorio público `malitox-code`.
2. Sube `index.html` y `README.md` a la raíz de `main` (no subas el ZIP sin extraer).
3. Settings → Pages → Deploy from a branch → main → /(root) → Save.
4. La URL esperada es `https://TU-USUARIO.github.io/malitox-code/` cuando termine el despliegue.

## IA real gratuita en tu PC (Ollama)

1. Instala Ollama desde su sitio oficial.
2. Descarga un modelo de código compatible, por ejemplo `ollama pull qwen2.5-coder:7b`. Requiere varios GB y puede ir lento según tu equipo.
3. Ejecuta Ollama y configura los orígenes CORS autorizados para la web según la documentación de Ollama (variable `OLLAMA_ORIGINS`).
4. Abre MALITOX CODE → ⚙ IA. URL: `http://localhost:11434/v1/chat/completions`, modelo: `qwen2.5-coder:7b`. No necesita clave en una instalación local estándar.

**Limitación importante:** según el navegador, GitHub Pages (HTTPS) puede bloquear solicitudes a un servidor HTTP local por CORS, seguridad o acceso a red local. Si eso ocurre, abre `index.html` localmente o usa un servidor HTTPS compatible. La página no contiene un backend de IA y no puede evadir esas restricciones.

## Seguridad

- La clave API se conserva solo en memoria durante la sesión, nunca en localStorage. No introduzcas claves privadas de pago en webs que no controles: el navegador y sus extensiones pueden acceder a ellas.
- Las sesiones y el código se guardan en `localStorage` de tu navegador. No se sincronizan entre equipos.
- Las respuestas se generan únicamente cuando hay una API conectada. Sin API, no hay respuestas falsas.
- El editor permite escribir, copiar, descargar y previsualizar HTML. No ejecuta terminales, plugins ni modifica archivos locales arbitrarios.

## Estado

Versión inicial funcional del frontend. No es una copia de DemonCode ni incluye su backend, su motor de agentes ni sus plugins.
