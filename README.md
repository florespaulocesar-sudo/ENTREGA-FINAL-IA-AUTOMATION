# INMOBILIARIA AI AUTOMATION

Automatización con n8n para la triage (clasificación) de consultas de clientes 
de una inmobiliaria, usando IA (OpenAI), Notion, Slack, Telegram y Gmail.

## Contenido de este repositorio

- **Diagrama de arquitectura**: `Aquitectura Entrega 8.pdf`
- **Lógica del flujo (archivo técnico)**: `LOGICA DEL FLUJO-JSON.pdf`
- **Descripción del proceso automatizado**: `DESCRIPCION DEL PROCESO AUTOMATIZADO.pdf`
- **Manual operativo de datos**: `manual_operativo_datos.pdf`
- **Optimización de costos**: `Cuadro comparativo- Costos.pdf`
- **Seguridad y resiliencia**: `seguridad_resiliencia.pdf`
- **Enlaces públicos**: `ENLACES PUBLICOS.pdf` (ver también la lista de abajo, con los links ya clickeables)
- **Capturas de pantalla del flujo**: `SCREENSHOTS DEL FLUJO CREADO_compressed.pdf`
- **Video de evidencia**: `Screen Recording 2026-09-29 r142600.mp4`

## Enlaces públicos (Notion)

1. Base de datos - Requerimientos: https://app.notion.com/p/3e49ebd3b3c080598857f894c9ce8cea?v=3e49ebd3b3c08016944e000c9cf9ef11&source=copy_link
2. Base de datos - Propiedades (RAG): https://app.notion.com/p/3e49ebd3b3c0806aa47be8c2671f797a?v=3e49ebd3b3c080eea30a000c63bb9e10&source=copy_link
3. Dashboard de control (KPIs y tasa de errores): https://app.notion.com/p/DASHBOARD-INMOBILIARIA-ENTREGA-8-3e79ebd3b3c080c4aef4e0879ebd949f?source=copy_link

## Resumen del flujo

El sistema recibe correos de clientes por Gmail, un agente de IA (GPT-4o-mini) 
interpreta la intención (compra, alquiler o consulta general) y calcula la 
prioridad del caso. Según la prioridad, el flujo notifica por Slack (para 
casos que requieren aprobación humana-prioridad Alta y Media) o responde automáticamente por Gmail 
(casos de prioridad Baja). Lo que no tiene que ver con comprar o alquilar un inmueble pasa como A_REVISAR. Un segundo circuito revisa periódicamente las 
aprobaciones humanas en Notion y responde al cliente por email y envía mensaje a Telegram de la inmobiliaria.
