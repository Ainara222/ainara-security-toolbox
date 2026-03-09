# 🚨 Auditoría y Gestión de Incidentes de Ciberseguridad

> **Eje Central del Proyecto:** Este módulo constituye el motor operativo para la identificación de amenazas, el análisis de vectores de ataque y la respuesta ante incidentes, integrando inteligencia de fuentes abiertas (OSINT) y monitorización avanzada.

---

## 📂 1. Taxonomía de Incidentes (Modelo INCIBE-CERT)
Para auditar con éxito, es vital hablar el mismo lenguaje que los centros de respuesta (CERT). Clasificamos los incidentes según su naturaleza:

| Categoría | Descripción y Ejemplos Clave |
| :--- | :--- |
| **Contenido Dañino** | Sistemas infectados con malware, botnets (C&C) y dominios DGA. |
| **Intento de Intrusión** | Explotación de vulnerabilidades conocidas (CVE), fuerza bruta o ataques 0-day. |
| **Intrusión** | Compromiso de cuentas (con/sin privilegios) y compromiso de aplicaciones (SQLi). |
| **Disponibilidad** | Ataques de denegación de servicio (DoS/DDoS) y sabotaje físico. |
| **Fraude** | Phishing, suplantación de identidad y uso no autorizado de recursos. |
| **Vulnerabilidad** | Criptografía débil, sistemas desactualizados o servicios expuestos (RDP, VNC). |



---

## 🔍 2. Detección y Alerta: Precursores vs. Indicadores
La auditoría proactiva depende de saber qué buscar antes y después de que ocurra el desastre:

* **Precursores (Indicios de futuro):**
    * Logs de escaneo de vulnerabilidades en el servidor web.
    * Anuncios de nuevos exploits para tecnologías usadas en la organización.
    * Amenazas en foros de hacktivismo.
* **Indicadores (Indicios de presente/pasado):**
    * Alertas de IDS/IPS (ej. Snort detectando desbordamientos de buffer).
    * Cambios inusuales en configuraciones de host o nombres de archivos extraños.
    * Desviaciones inusuales en el tráfico de red (exfiltración de datos).

---

## 📡 3. Inteligencia de Fuentes Abiertas (OSINT)
El proceso OSINT es fundamental en la fase de reconocimiento de una auditoría para identificar qué sabe un atacante sobre nosotros.

### Fases del Proceso OSINT
1. **Requisitos:** Definir el objetivo.
2. **Identificación:** Localizar fuentes relevantes.
3. **Adquisición:** Obtención de los datos.
4. **Procesamiento:** Dar formato a la información.
5. **Análisis:** Relacionar datos para encontrar patrones.
6. **Presentación:** Generar inteligencia accionable.

### Toolbox de Auditoría OSINT
* **Reconocimiento de Red:** `Shodan` (dispositivos IoT, cámaras, servidores expuestos).
* **Identidades:** `NameCHK` / `Knowem` (presencia en redes sociales).
* **Infraestructura:** `TheHarvester` (emails, subdominios), `Domaintools`.
* **Metadatos:** `Metagoofil` (extracción de info oculta en PDFs, DOCs).
* **Visualización:** `Maltego` (relaciones gráficas entre entidades).

---

## 🛡️ 4. Infraestructura de Respuesta: SOC, SIEM e IDS
El corazón de la gestión de incidentes es la **Detección Temprana**.

### El Trípode de la Respuesta:
1.  **IDS/IPS (ej. Snort):** Actúa como el sensor. Detecta intrusiones mediante firmas y puede bloquear el tráfico sospechoso en tiempo real.
2.  **SIEM (Security Information and Event Management):** El cerebro que centraliza logs de firewalls, servidores y aplicaciones, permitiendo correlacionar eventos para detectar ataques complejos (APT).
3.  **Análisis Forense (ej. Volatility):** Si la prevención falla, realizamos el análisis post-mortem de la RAM para entender la causa raíz y extraer artefactos del atacante.



---

## 🧱 5. Auditoría de Seguridad Física y del Entorno (ISO 27001)
No toda la ciberseguridad es lógica. La seguridad física es el primer perímetro:
* **Áreas Seguras:** Control de acceso físico, protección contra desastres ambientales y seguridad en oficinas/Carga-Descarga.
* **Seguridad de los Equipos:** Protección del cableado (evitar interceptaciones), mantenimiento preventivo y **eliminación segura** de soportes (destrucción de datos sensibles).
* **Política de Pantalla Limpia:** Obligatoriedad de bloquear equipos y no dejar documentos sensibles a la vista.

---

## 📈 6. Modelo de Mejora Continua (AS IS / TO BE)
Toda auditoría debe concluir con una hoja de ruta:
1.  **AS IS:** ¿Cuál es nuestro nivel de seguridad actual? (Auditoría inicial).
2.  **TO BE:** ¿Qué nivel queremos alcanzar basándonos en el riesgo?
3.  **Kaizen:** Implementación de ciclos de revisión cada 6 meses o tras cambios significativos.

---

## 🛠️ Laboratorio de Auditoría (Hitos del Proyecto)
* **Simulación de Vectores:** Creación de shells inversas mediante exploits para entender la post-explotación.
* **Pruebas de Phishing:** Uso de *Phishers* para evaluar la concienciación de los usuarios.
* **Diccionarios Dinámicos:** Generación de ataques de fuerza bruta con `Hydra` y `Crunch` para auditar la robustez de las contraseñas.
