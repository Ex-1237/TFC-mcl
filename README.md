# TFC: Sistema RAG de Auditoría de Cumplimiento Normativo

Proyecto desarrollado en el marco del TFC 2026. Este repositorio contiene la implementación de un agente de IA especializado en la auditoría automatizada de políticas corporativas frente a marcos regulatorios internacionales (ENS, ISO 27001, GRPD).

##  Descripción del Proyecto
El sistema utiliza una arquitectura **RAG (Retrieval-Augmented Generation)** orquestada mediante **n8n** para analizar documentos internos de MIDTECH S.A. y contrastarlos con normativas externas. El objetivo es identificar brechas de cumplimiento de forma automatizada y eficiente.
##  Estructura del Repositorio
*   `README.md`: Documentación del proyecto.
* PDFs usados
*   accesso al Webhook y chatbot

##  Arquitectura Técnica
*   **Orquestación:** n8n Workflow (Pipeline de procesamiento de datos).
*   **Procesamiento de Lenguaje (LLM):** Google Gemini 2.5 Flash-Lite.
*   **Gestión de Documentos:** Google Drive API (Sincronización de políticas).
*   **Almacenamiento:** Gestión de contexto en memoria para validación en tiempo real.

##  Configuración y Ejecución
El sistema está diseñado para una gestión dinámica del conocimiento mediante dos modalidades:

### 1. Inicialización Manual
Desde el editor de n8n, se debe ejecutar el flujo para cargar el contexto actualizado desde Google Drive:
*   Abrir `TFC-MCL` en n8n.
*   Hacer clic en **"Execute Workflow"**.

### 2. Automatización (Webhook)
El proyecto incluye un punto de entrada API para integraciones de CI/CD o disparadores automáticos.
*   **Método:** POST
*   **Endpoint:** https://mcld.app.n8n.cloud/webhook/569cdacf-3c59-4c7b-8ae1-2502f73553b4
*   **Estado:** El workflow debe estar en modo **[Active]** para escuchar peticiones externas.

##  Acceso al Sistema / Chatbot
Puede realizar pruebas funcionales del agente de cumplimiento a través del siguiente enlace:

 **[Acceder al Chatbot de Auditoría (TFC)](https://mcld.app.n8n.cloud/webhook/c3ba3f0a-f587-47c2-890d-    04745a706629/chat )**
---

