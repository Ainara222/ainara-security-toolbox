# Análisis Forense Informático: Fundamentos y Metodología

> **ID:** NDC-AFI-01  
> **Tema:** Introducción al Análisis Forense Digital (DFIR)  
> **Caso Práctico:** Investigación de Ciberataque a Entidad Financiera (ACME Bank)

---

## 📖 1. Introducción al Análisis Forense
El **Análisis Forense Informático** se define como el conjunto de técnicas y procedimientos para extraer evidencias de soportes digitales sin alterar su estado original. En una sociedad digitalizada, es una disciplina crítica tanto para requerimientos judiciales como para la respuesta ante incidentes (DFIR).



### El Objetivo Principal
No es simplemente recolectar datos, sino **contar una historia** basada en hechos. Para reconstruir los sucesos, un analista debe responder a las "5 Ws":
* **What?** (¿Qué ha sucedido realmente?)
* **Where?** (¿En qué sistemas o redes?)
* **Who?** (¿Quiénes son los responsables?)
* **When?** (¿Cuál es la línea temporal exacta?)
* **Why/How?** (¿Qué motivación y herramientas se usaron?)

---

## 🏢 2. Caso Práctico: El primer caso de María
**Contexto:** María, analista del equipo DFIR, debe investigar un ataque contra una entidad financiera donde se ha robado dinero y varios sistemas han quedado inoperativos.

**Escenarios que enfrentará:**
1.  **Escenario Judicial:** Centrado en la documentación exhaustiva y la cadena de custodia para que las pruebas sean válidas ante un juez. Requiere la presencia de un notario.
2.  **Escenario de Respuesta a Incidentes:** Centrado en la rapidez para mitigar la amenaza y entender la motivación del ataque.

---

## 📋 3. Metodología Forense
Para que el trabajo sea válido, debe cumplir con las siguientes características:

| Característica | Descripción |
| :--- | :--- |
| **Verificable** | Se debe poder comprobar la veracidad de las conclusiones con datos objetivos. |
| **Reproducible** | Otro perito debe poder llegar a los mismos resultados siguiendo el mismo proceso. |
| **Documentado** | Registro detallado y comprensible de cada acción sobre la evidencia. |
| **Independiente** | Las conclusiones deben ser objetivas, sin importar quién realice el análisis. |

### Fases del Análisis
1. **Identificación:** Localizar dispositivos físicos (móviles, discos) y fuentes lógicas (logs, RAM).
2. **Adquisición:** Realizar una copia fiel de la información original.
3. **Preservación:** Garantizar la integridad mediante la cadena de custodia.
4. **Análisis:** Procesar las evidencias y crear la línea de tiempo (*timeline*).
5. **Presentación:** Elaborar el informe técnico y el resumen ejecutivo.

---

## 🕵️ 4. Identificación y Adquisición
### Orden de Volatilidad
En la fase de adquisición, es vital recolectar primero la información que desaparece más rápido:

1.  **Registros de CPU y Caché de memoria.**
2.  **Memoria RAM**, tabla ARP, tabla de procesos, archivos temporales.
3.  **Discos duros** y dispositivos de almacenamiento externo.
4.  **Configuraciones físicas** y topologías de red.



### Cadena de Custodia
Garantiza que lo analizado es lo mismo que lo incautado. Debe incluir:
* Identificación unívoca (Marca, modelo, número de serie).
* Timestamp de recogida.
* Localización física y responsable de la custodia.
* Documentación de cada cambio de mano de la evidencia.

---

## 🛠️ 5. Herramientas del Analista
Los analistas utilizan un "maletín forense" que incluye tanto hardware como software especializado.

### Hardware
* **Bloqueadores de escritura (Write Blockers):** Impiden que se escriba nada en el disco original durante la copia.
* Hardware de clonado de discos (SATA, IDE, USB, etc.).

### Software por tipo de análisis
* **Memoria RAM:** Volatility.
* **Discos:** EnCase, FTK Suite, Magnet Forensics.
* **Dispositivos Móviles:** Cellebrite.
* **Análisis de Logs:** SIEMs (Splunk), Grep/Cut (Unix), PowerShell, GoAccess.

---

## 📝 6. El Informe Forense (Reporte)
El resultado final se divide en dos grandes bloques:

1.  **Resumen Ejecutivo:** Dirigido a la gerencia, explica los hechos y conclusiones a alto nivel sin tecnicismos excesivos.
2.  **Desglose Técnico:** Detalle minucioso de cada fase, herramientas usadas, evidencias halladas y la **Línea de Tiempo (Timeline)** de los hechos.

---

## 💡 Autoevaluación
**Pregunta:** ¿Cuál de las siguientes fuentes de información debería recolectarse primero?
* A) Disco externo USB
* **B) Memoria RAM del ordenador** (Correcta: Es altamente volátil y se pierde al apagar).
* C) CD-ROM
* D) Fichero dentro del ordenador

---

## 🔗 Referencias y Guías de Buenas Prácticas
* **UNE-EN ISO/IEC 27037:2016:** Guía para la identificación, recogida, adquisición y preservación de evidencias digitales.
* **UNE 71506:2013:** Metodología para el análisis forense de evidencias electrónicas.
* **Electronic Crime Scene Investigation:** Guía de referencia para escenas del crimen.
