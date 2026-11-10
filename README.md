# Trazo — demostración gratuita

Web estática para convertir una conversación en diagramas de flujo,
arquitectura lógica y casos de uso. No hay cuentas de usuario, pagos ni API
de inferencia: el audio y el texto se procesan en el navegador.

## Uso

1. Abre la web en Chrome o Edge actualizado, con aceleración gráfica.
2. Pulsa **Activar IA gratuita**. La primera descarga de Qwen3 ocupa unos 2,5 GB.
3. Escribe el proceso o pulsa **Empezar a escuchar**. La voz descarga Whisper
   la primera vez y solicita permiso para usar el micrófono.
4. Revisa las evidencias, corrige el contexto y genera las vistas que necesites.

Modelo de interpretación: `Qwen3-4B-q4f16_1-MLC`, mediante WebLLM/WebGPU.
Voz: `onnx-community/whisper-base`, cuantización q8 y WebAssembly.

Se necesita WebGPU con `shader-f16` y memoria suficiente. Se recomienda un
ordenador con 16 GB de RAM; no se garantiza compatibilidad con todos los móviles.
Si el dispositivo no admite la IA, el editor manual sigue disponible. El
rendimiento depende del equipo y la IA puede interpretar mal la conversación.

## Privacidad y límites

El alojamiento solo sirve archivos. Los modelos se descargan de repositorios
públicos; no se les envía la conversación ni el audio. Las reuniones se guardan
en este navegador. Exporta JSON para conservarlas o moverlas desde la versión
de localhost. El navegador puede liberar los modelos en caché.

No hay un servidor local que instalar ni un servidor de IA en la nube que pagar.
El dispositivo del visitante aporta cómputo, electricidad, almacenamiento y la
descarga inicial. No es una promesa de recursos físicos ilimitados.

Esta publicación es una demostración, no un servicio comercial. GitHub Pages
tiene [límites y condiciones de uso](https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits).
No se deben realizar transacciones sensibles ni alojar un SaaS comercial aquí.

## Atribuciones

`THIRD-PARTY-NOTICES.txt` conserva las licencias de las dependencias distribuidas.
Los pesos no forman parte de este repositorio. Qwen3 está bajo Apache 2.0 y
Whisper bajo MIT; consulta también las fichas originales:

- https://huggingface.co/mlc-ai/Qwen3-4B-q4f16_1-MLC
- https://huggingface.co/onnx-community/whisper-base
- https://github.com/mlc-ai/web-llm
- https://github.com/huggingface/transformers.js
