# MALITOX CODE V2 — Multi IA

## Publicar en GitHub Pages
1. Crea un repositorio público `malitox-code`.
2. Sube `index.html` a la raíz del repositorio (y este README opcionalmente).
3. Settings → Pages → Deploy from a branch → main → /(root) → Save.
4. Abre `https://TU-USUARIO.github.io/malitox-code/`.

## Conectar un modelo local gratis
1. Instala Ollama desde su web oficial.
2. Abre PowerShell y ejecuta `ollama pull qwen2.5-coder:7b`.
3. Para permitir peticiones desde tu sitio de GitHub Pages, configura la variable de entorno `OLLAMA_ORIGINS` con `https://TU-USUARIO.github.io` y reinicia Ollama. Consulta la documentación oficial de Ollama para configurarla en Windows. No abras Ollama a internet.
4. En MALITOX CODE, abre Configurar IA, elige Ollama, API `http://localhost:11434/v1/chat/completions`, modelo `qwen2.5-coder:7b`, y Conectar.
5. Si el navegador bloquea peticiones de GitHub Pages a localhost por políticas de red o seguridad, prueba abriendo el archivo `index.html` localmente o usando un proxy privado de confianza. GitHub Pages no ejecuta modelos.

## Proveedores online
Puedes elegir OpenRouter, Groq o una API compatible con OpenAI. Debes usar tu propia cuenta, clave y un identificador de modelo válido. Algunos modelos tienen planes gratuitos con cuotas. Las API pueden bloquear peticiones directas desde navegadores (CORS). Nunca guardes una clave secreta en el código público de GitHub.

## Qué funciona
- Conversaciones, historial en localStorage, selector de modelo, peticiones reales al endpoint OpenAI-compatible, editor, extracción de primer bloque de código, copia, descarga y vista previa HTML aislada.
- La clave de API permanece solo en memoria de la pestaña y se borra al recargar.

## Límites
- No es una IA entrenada por MALITOX: las respuestas provienen del modelo que conectes.
- No ejecuta código del servidor ni modifica repositorios automáticamente.
- No incluye claves de pago ni conexiones a servicios sin autorización.
- El editor es básico y el visor HTML solo sirve para pruebas de páginas no confiables con sandbox.
- Los modelos locales requieren RAM y CPU/GPU suficientes; 7B puede ser lento en equipos modestos.
