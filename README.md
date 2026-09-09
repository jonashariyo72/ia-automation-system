🚀 Entrega Final: Ecosistema de Automatización IA Autónomo para Negocios

Alumno: Jonás Hariyo | Curso: AI Automation - CoderHouse

📌 Descripción del Proyecto
Ecosistema de automatización de extremo a extremo que resuelve el proceso de generación, enriquecimiento contextual (RAG), validación humana (Human-in-the-Loop) y distribución de contenidos corporativos B2B.

🏗️ Arquitectura e Integraciones
* **Orquestador:** Make (Integromat)
* **Base de Datos Relacional:** Airtable (Pipeline de Contenidos)
* **Procesamiento de IA:** Make AI Toolkit (Simple Text Prompt / RAG B2B)
* **Canal de Salida:** Gmail API

🔗 Enlaces Obligatorios de la Entrega
* 📊 **Base de Datos Operativa (Lectura Pública):** [Ver Base Airtable](link_a_airtable)
* 🎥 **Video Demo (3 min):** [Ver Video en Loom/YouTube](link_al_video)

🛡️ Resiliencia y Seguridad
* **Human-in-the-Loop (HITL):** Filtro booleano estricto (Aprobado = TRUE y Estado = Pendiente) que detiene la ejecución antes del envío final por Gmail.
* **Gestión de Errores:** Directiva Resume en el nodo de IA para tolerancia a fallos por límite de cuotas (Rate Limit 429).
* **Idempotencia:** Control de estados en Airtable (Generando → Pendiente → Publicado) para prevenir envíos duplicados o bucles infinitos.

📊 Matriz de Optimización Financiera y Selección de LLM
| Modelo Evaluado | Costo (Input/Output por 1M tokens) | Latencia | Caso de Uso Ideal | Veredicto para este Pipeline |
| :--- | :--- | :--- | :--- | :--- |
| **GPT-4o / Claude 3.5 Sonnet** | Alto (~$5.00 / ~$15.00) | Media | Razonamiento complejo, análisis profundo. | **Descartado**. Excesivo para redacción de borradores; encarece el costo operativo. |
| **GPT-4o-mini / Claude 3 Haiku** | Bajo (~$0.15 / ~$0.60) | Muy Baja (Rápido) | Tareas repetitivas, redacción de textos cortos, clasificación. | **Seleccionado**. Óptima relación costo/rendimiento para la generación automatizada en lote. |

📂 Archivos Adjuntos en el Repositorio
* **Entrega_Final_AI_Automation_OFICIAL.pdf:** Documentación técnica completa (incluyendo los esquemas JSON de integración de APIs).
* **blueprint.json:** Flujo exportado de Make validado y listo para importar.
* **Interfaz.pdf:** Reporte visual exportado que evidencia el Dashboard de KPIs, métricas generales y gráficos de distribución.
