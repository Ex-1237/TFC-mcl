# TFC: Sistema RAG de Auditoría de Cumplimiento Normativo

Proyecto desarrollado en el marco del TFC 2026. Este repositorio contiene la implementación de un agente de IA especializado en la auditoría automatizada de políticas corporativas frente a marcos regulatorios internacionales (ENS, ISO 27001, GRPD).

##  Descripción del Proyecto
El sistema utiliza una arquitectura **RAG (Retrieval-Augmented Generation)** orquestada mediante **n8n** para analizar documentos internos de MIDTECH S.A. y contrastarlos con normativas externas. El objetivo es identificar brechas de cumplimiento de forma automatizada y eficiente.
##  Estructura del Repositorio
*   `README.md`: Documentación del proyecto.
*
*   

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
*   **Endpoint:** `[Production URL  - hier eintragen`
*   **Estado:** El workflow debe estar en modo **[Active]** para escuchar peticiones externas.

##  Acceso al Sistema / Chatbot
Puede realizar pruebas funcionales del agente de cumplimiento a través del siguiente enlace:

 **[Acceder al Chatbot de Auditoría (TFC)](LINK kommt noch)**
---
*creado por [Ex-1237]((https://github.com/Ex-1237))*
