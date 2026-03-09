# Diseño de Planes de Securización y Bastionado

> **Caso Práctico:** Modernización de la clínica "Venus SA".  
> **Objetivo:** Transformación digital segura: de historiales físicos a un sistema gestionado y protegido.

---

## 🏗️ 1. Proyecto de Modernización (Venus SA)
Para digitalizar la clínica, el CEO ha definido los siguientes hitos:
* **Desarrollo de Software:** Gestión de historiales, nóminas y proveedores.
* **Informatización:** Migración total de datos físicos a soporte digital.
* **Infraestructura:** Compra de servidores y puestos de trabajo.
* **Presencia Digital:** Página web corporativa.
* **Restricción Crítica:** Presupuesto reducido y plazos de entrega agresivos.

---

## 🔍 2. Análisis de Riesgos
El primer paso de cualquier plan de securización es conocer la situación de partida. No se puede proteger lo que no se identifica.

### Fases del Análisis
1. **Reconocimiento Inicial:** Identificar el nivel de madurez, activos técnicos y cumplimiento normativo (RGPD).
2. **Alcance:** Definir qué áreas son críticas (ej. el área de I+D+i o la base de datos de pacientes).
3. **Identificación de Amenazas:** Evaluar la probabilidad de que ocurra un evento dañino.
   * **Cálculo de Riesgo:** $Riesgo = Impacto (€) \times Probabilidad$
   
4. **Tratamiento del Riesgo:**
   * **Mitigar:** Implementar controles.
   * **Eliminar:** Cesar la actividad que genera el riesgo.
   * **Transferir:** Contratar un ciberseguro.
   * **Aceptar:** Asumir el riesgo residual.

### Escala de Madurez (CMM)
* **Inexistente:** Sin políticas.
* **Inicial:** Sin planificación ni control.
* **Definido:** Procedimientos claros pero no aprobados formalmente.
* **Optimizado:** Mejora continua basada en indicadores (KPIs).

---

## ♻️ 3. Economía Circular en IT
Principios para un sistema productivo sostenible en la industria 4.0:
* **Residuo como recurso:** Reutilización de materiales biodegradables y técnicos.
* **Mantenimiento:** Alargar la vida útil para evitar la obsolescencia programada.
* **Eco-diseño:** Integrar el impacto medioambiental desde la concepción del sistema.

---

## 🛠️ 4. Medidas Técnicas de Seguridad
Las herramientas se dividen en dos grandes bloques operativos:

### A. Medidas Preventivas (Evitar la infección/ataque)
* **Antimalware (EDR/XDR):** Soluciones avanzadas con inteligencia artificial.
* **Firewalls:** Control de tráfico entre redes.
* **DLP (Data Loss Prevention):** Herramientas para evitar la fuga de datos.
* **Virtual Patching:** Protección de sistemas obsoletos que no pueden actualizarse físicamente.
* **SIEM:** Centralización y análisis de eventos de seguridad.



### B. Medidas Reactivas (Contener y recuperar)
* **IPS (Intrusion Prevention System):** Bloqueo activo tras detectar una intrusión.
* **Plan de Contingencia:** Procedimiento de restauración de la actividad.
* **Backups:** Copias de seguridad, esenciales para la continuidad de negocio.

---

## 📋 5. Políticas y Estándares de Securización
Es fundamental diferenciar entre **Buenas Prácticas** (recomendaciones) y **Políticas** (obligatorias y sancionables).

### Estándares de Referencia
| Estándar | Descripción |
| :--- | :--- |
| **ISO/IEC 27001** | Requisitos para un SGSI (Sistema de Gestión de Seguridad). |
| **NIST CSF** | Marco de trabajo enfocado en: Identificar, Proteger, Detectar, Responder y Recuperar. |
| **ENS** | Esquema Nacional de Seguridad (España), clave para trabajar con la administración pública. |

---

## 🔄 6. Caracterización de Procesos
Para que un servicio de seguridad (como un SOC) funcione, debe caracterizar sus procesos:
* **Entradas (Inputs):** Logs, alertas, llamadas de usuarios.
* **Procesado:** Análisis mediante herramientas como RTIR o Sandboxes.
* **Salidas (Outputs):** Informes, estadísticas, cierre de incidentes.
* **Indicadores:** Métricas (KPIs) para medir la eficacia del proceso.



---

## ⚠️ 7. Gestión y Escalado de Incidentes
Definiciones clave para el triaje:
1. **Evento:** Cambio de estado significativo en la red.
2. **Evento de Seguridad:** Violación de una política de seguridad.
3. **Incidente:** Evento que pone en riesgo real los activos de la organización.

### Niveles de Atención
* **Nivel 1:** Resolución técnica inicial, seguimiento de alertas comunes.
* **Nivel 2:** Escalado para incidentes complejos o críticos (ej. Ransomware activo).

---

## 💡 Autoevaluación
* **¿Cuál es la fase inicial del análisis de riesgos?** El reconocimiento inicial de la situación actual.
* **¿Es lo mismo una política que una buena práctica?** No. La política es de obligado cumplimiento; la buena práctica es una recomendación.
