# 🚀 Ecosistema de Automatización de Contenidos B2B (AI + HITL)

**Alumno:** Jonás Hariyo
**Curso:** AI Automation - CoderHouse  

---

## 📌 Descripción del Proyecto
Ecosistema de automatización de extremo a extremo que resuelve el proceso de generación, enriquecimiento contextual (RAG), validación humana (*Human-in-the-Loop*) y distribución de contenidos corporativos B2B.

---

## 🏗️ Arquitectura e Integraciones
* **Orquestador:** Make (Integromat)
* **Base de Datos Relacional:** Airtable (`Pipeline de Contenidos`)
* **Procesamiento de IA:** Make AI Toolkit (Simple Text Prompt / RAG B2B)
* **Canal de Salida:** Gmail API

---

## 🔗 Enlaces Obligatorios de la Entrega

* 📊 **Dashboard de Control (Shared View Público):** [Ver Panel de KPIs en Airtable](PEGA_AQUI_TU_LINK_DE_AIRTABLE)
* 🗄️ **Base de Datos (Lectura Pública):** [Ver Base Airtable](PEGA_AQUI_EL_LINK_DE_TU_BASE)
* 🎥 **Video Demo (3 min):** [Ver Video en Loom/YouTube](PEGA_AQUI_EL_LINK_DEL_VIDEO)

---

## 🛡️ Resiliencia y Seguridad
- **Human-in-the-Loop (HITL):** Filtro booleano estricto (`Aprobado = TRUE` y `Estado = Pendiente`) que detiene la ejecución antes del envío final por Gmail.
- **Gestión de Errores:** Directiva `Resume` en el nodo de IA para tolerancia a fallos por límite de cuotas (Rate Limit 429).
- **Idempotencia:** Control de estados en Airtable (`Generando` → `Pendiente` → `Publicado`) para prevenir envíos duplicados o bucles infinitos.

---

## 📂 Archivos Adjuntos en el Repositorio
- `Entrega_Final_AI_Automation_OFICIAL.pdf`: Documentación técnica completa respondiendo a los 5 criterios de la rúbrica.
- `blueprint.json`: Flujo exportado de Make listo para importar.
- `/img`: Capturas de pantalla con evidencias del testeo en vivo.
