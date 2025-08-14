# 🛡 Laboratorio de Hacking Ético – Metasploitable 3 Ubuntu 14.04 LTS  

## Descripción  
Este laboratorio simula un escenario controlado de pruebas de penetración (*pentest*) sobre un sistema vulnerable, siguiendo una metodología estándar desde el reconocimiento hasta la escalada de privilegios.  
El objetivo es poner en práctica técnicas y herramientas de **ciberseguridad ofensiva** en un entorno seguro.  

⚠️ **Aviso legal:** Todo el ejercicio se realizó en un laboratorio aislado, sin afectar sistemas externos, con fines exclusivamente educativos.  

---

##  Entorno de Trabajo  
- **Atacante:** Kali Linux (VirtualBox 7.1.10)  
- **Objetivo:** Metasploitable 3 – Ubuntu 14.04 LTS  
- **Red:** Host-Only – `192.168.56.0/24`  
- **Herramientas principales:**  
  - `Nmap`  
  - `Nessus Essentials`  
  - `Metasploit Framework`  
  - `Docker`  
  - `Python`  

---

## Metodología  
1. **Reconocimiento de hosts** – Descubrimiento de IPs activas.  
2. **Escaneo de puertos y servicios** – Identificación de software y versiones.  
3. **Análisis de vulnerabilidades** – Uso de Nmap NSE y Nessus para priorizar fallos críticos.  
4. **Explotación** – Uso de `exploit/unix/irc/unreal_ircd_3281_backdoor` para RCE.  
5. **Escalada de privilegios** – Abuso de permisos en grupo `docker` para obtener `root`.  

---

## Vulnerabilidades clave encontradas  

UnrealIRCd Backdoor - CVE-2010-2075 - Crítica - Versión troyanizada con ejecución remota de comandos sin autenticación.
Drupal Coder Module RCE - Plugin 92626 - Crítica - Deserialización insegura que permite RCE.
MySQL Expuesto - Alta - Servicio accesible sin restricción externa. 

---

## Evidencias  
En el PDF incluido se documentan:  
- Resultados de escaneo de red y servicios.  
- Salidas de Nmap y Nessus.  
- Ejecución del exploit y obtención de shell.  
- Escalada de privilegios a root vía Docker.  

---

## Documentación completa  
📂 **[Laboratorio_Hacking_Etico.pdf](Laboratorio%20Hacking%20Etico.pdf)**  

---

## Recomendaciones de remediación  
- **Actualizar UnrealIRCd** a versión libre de backdoor.  
- **Eliminar usuarios no administradores** del grupo `docker`.  
- **Actualizar SO** a una versión con soporte.  
- **Revisar configuraciones SSL/TLS** para deshabilitar cifrados débiles.  

---

## Autor  
**Ivan Fibiger** – Técnico Universitario en Tecnologías de Programación | En proceso de formación en Ciberseguridad.  
