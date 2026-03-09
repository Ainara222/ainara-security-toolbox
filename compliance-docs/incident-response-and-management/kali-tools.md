# 🛠️ Cybersecurity Audit: Command Reference Guide

Este fichero centraliza los comandos esenciales para la fase de **reconocimiento, análisis de red y auditoría de sistemas**. Es mi guía rápida de referencia para ejecutar herramientas de seguridad directamente desde la terminal.

---

## 🔍 1. Nmap (Network Mapper)
El estándar para descubrimiento de hosts y auditoría de servicios.


* **Escaneo rápido de red:**
  `nmap -sn 192.168.1.0/24` (Descubrimiento de hosts vivos sin escanear puertos).
* **Escaneo de servicios y versiones (Agresivo):**
  `nmap -sV -sC -A 192.168.1.45` (Detecta versiones, ejecuta scripts básicos y hace OS Detection).
* **Escaneo de todos los puertos (65535):**
  `nmap -p- --min-rate 5000 192.168.1.45` (Rápido y exhaustivo).
* **Auditoría de vulnerabilidades con scripts (NSE):**
  `nmap --script vuln 192.168.1.45` (Busca CVEs conocidos en el target).

---

## 🛰️ 2. Enumeración y Reconocimiento
Comandos para identificar qué hay "ahora mismo" en el sistema o la red.

* **Netstat / SS (Conexiones activas):**
  `ss -tunlp` (Muestra puertos escuchando, procesos y protocolos UDP/TCP).
* **Netdiscover (ARP Scanning):**
  `sudo netdiscover -i eth0 -r 192.168.1.0/24` (Ideal para descubrir dispositivos en red local).
* **Dig (DNS Audit):**
  `dig axfr @ns1.target.com target.com` (Intento de transferencia de zona para listar subdominios).

---

## 🛡️ 3. Auditoría de Sistemas (Hardening & Analysis)
Comandos para revisar la seguridad interna del host (Local Audit).

* **UFW (Firewall de Ubuntu):**
  `sudo ufw status numbered` / `sudo ufw allow 22/tcp` (Gestión de reglas de acceso).
* **Journalctl (Análisis de logs en caliente):**
  `journalctl -u ssh -f` (Monitorización en tiempo real de intentos de acceso por SSH).
* **Permisos Críticos (SUID):**
  `find / -perm -u=s -type f 2>/dev/null` (Busca binarios que se ejecutan con privilegios de root).

---

## 🧪 4. Herramientas de Explotación Ética
Comandos rápidos para herramientas de auditoría de credenciales y servicios.

* **Hydra (Fuerza Bruta):**
  `hydra -l admin -P /usr/share/wordlists/rockyou.txt ssh://192.168.1.45` (Ataque de diccionario contra SSH).
* **John the Ripper (Cracking de hashes):**
  `john --wordlist=/usr/share/wordlists/rockyou.txt hashes.txt` (Auditoría de robustez de contraseñas).
* **TheHarvester (OSINT):**
  `theHarvester -d target.com -b google` (Extracción de emails y subdominios de fuentes públicas).

---

## 🐍 5. Integración con Scripts de Python
Para ejecutar mi **NVD/NIST Scanner** y otras utilidades propias:

* **Ejecución del escáner de vulnerabilidades:**
  `python3 nvd_scanner.py --list dependencies.txt --severity HIGH`

---
> **Tip Pro:** Usa `grep` o `awk` para filtrar los resultados de estos comandos y enviarlos directamente a un reporte `.txt` o `.md` para tu auditoría.