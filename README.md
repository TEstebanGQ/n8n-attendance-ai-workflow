# 📌 Sistema Automatizado de Gestión de Inasistencias

## 🧩 Descripción General

Este proyecto propone el desarrollo de un sistema automatizado para la gestión, análisis y clasificación de solicitudes de justificación de inasistencias en entornos educativos.

Actualmente, este proceso suele realizarse de forma manual, lo que lo hace lento, propenso a errores y difícil de escalar. Esta solución integra automatización de procesos e inteligencia artificial para optimizar tiempos de respuesta, reducir la carga operativa y mejorar la trazabilidad de las solicitudes.

---

## 🎯 Objetivos

### Objetivo General
Desarrollar un sistema automatizado que permita registrar, analizar y gestionar solicitudes de justificación de inasistencias.

### Objetivos Específicos
- Diseñar un formulario web para la recepción de solicitudes.
- Automatizar el almacenamiento de datos en Google Sheets.
- Implementar un sistema de análisis automático mediante IA.
- Clasificar solicitudes en válidas, inválidas o pendientes.
- Integrar un bot de Telegram para consulta de estado.
- Reducir el tiempo de respuesta en validaciones.
- Incorporar revisión manual para casos ambiguos.

---

## 🏗️ Arquitectura del Sistema

El sistema sigue el siguiente flujo:

1. El usuario completa un formulario web.
2. Los datos son enviados a través de un webhook.
3. n8n procesa la información y archivos adjuntos.
4. El módulo de IA analiza el contenido (incluyendo OCR).
5. Se clasifica la solicitud y se asigna un nivel de confianza.
6. Se toma una decisión automática o se envía a revisión.
7. Los datos se almacenan en Google Sheets.
8. El usuario recibe notificaciones vía Telegram.

---

## ⚙️ Componentes del Sistema

### 📄 Formulario Web
Permite al estudiante:
- Ingresar datos personales.
- Seleccionar motivo de inasistencia.
- Adjuntar documentos o imágenes de soporte.

---

### 🔄 Motor de Automatización (n8n)
Responsable de:
- Recepción de datos mediante webhook.
- Procesamiento de archivos.
- Integración con servicios de IA.
- Automatización de decisiones.
- Envío de notificaciones.

---

### 🤖 Módulo de Inteligencia Artificial
Funciones principales:
- Análisis del contenido del documento.
- Extracción de texto (OCR).
- Clasificación de la solicitud:
  - Válida
  - Inválida
  - Dudosa
- Asignación de nivel de confianza.

---

### 📊 Sistema de Almacenamiento (Google Sheets)
Registra:
- Datos del estudiante.
- Estado de la solicitud.
- Resultado del análisis.
- Historial completo.

---

### 💬 Bot de Telegram
Permite:
- Consultar estado de solicitudes mediante ID.
- Recibir notificaciones automáticas.
- Visualizar historial personal.

---

### 🧠 Sistema de Decisión

Basado en niveles de confianza:

| Nivel de Confianza | Acción |
|-------------------|--------|
| Alta              | Aprobación/Rechazo automático |
| Media             | Revisión manual |
| Baja              | Rechazo o solicitud de información adicional |

---

## 🚀 Funcionalidades Adicionales

- Extracción automática de texto (OCR).
- Identificación de palabras clave.
- Detección de documentos duplicados.
- Validación de formatos de archivo.
- Historial por estudiante.
- Panel básico de métricas.
- Sistema de logs y monitoreo de errores.

---

## ⚠️ Riesgos y Limitaciones

- Posibles errores en la clasificación por IA.
- Dificultad para detectar documentos falsificados.
- Dependencia de servicios externos.
- Necesidad de supervisión humana en casos críticos.

---

## 📈 Resultados Esperados

- Reducción significativa del tiempo de validación.
- Disminución de carga operativa manual.
- Mayor trazabilidad de las solicitudes.
- Mejora en la experiencia del usuario.
- Sistema escalable y eficiente.

---

## 🧪 Tecnologías Sugeridas

- n8n (automatización)
- Google Sheets (almacenamiento)
- API de IA (procesamiento de lenguaje e imágenes)
- OCR (reconocimiento de texto)
- Telegram Bot API
- Webhooks

---

## 📌 Conclusión

Este sistema representa una solución moderna y eficiente para la gestión de inasistencias en instituciones educativas. La integración de automatización e inteligencia artificial permite optimizar procesos administrativos, mejorar la toma de decisiones y ofrecer una experiencia ágil tanto para estudiantes como para el personal administrativo.

---

## 👨‍💻 Autor

tomas