# Proyecto Final – Fundamentos de Enrutamiento

## 📌 Introducción

En este repositorio se presenta el desarrollo del proyecto final de la asignatura **Fundamentos de Enrutamiento**, en el cual se implementó una red completa simulada en Cisco Packet Tracer.

El objetivo principal fue aplicar de manera práctica los conocimientos adquiridos durante el cuatrimestre, integrando múltiples tecnologías y protocolos de red para construir una infraestructura funcional, escalable y redundante.

Durante este proyecto se configuraron routers, switches, servidores y dispositivos inalámbricos, logrando la comunicación entre diferentes segmentos de red mediante el uso de VLANs, enrutamiento, servicios de red y mecanismos de alta disponibilidad.

---

## 🎯 Objetivos del Proyecto

* Implementar una red segmentada utilizando VLANs.
* Configurar enrutamiento entre redes (Inter-VLAN Routing).
* Aplicar protocolos de redundancia para alta disponibilidad.
* Implementar servicios como DHCP, DNS y autenticación.
* Configurar conectividad WAN entre múltiples routers.
* Integrar red cableada e inalámbrica.

---

## 🌐 Protocolos y Tecnologías Implementadas

### 🔹 VLAN (Virtual Local Area Network)

Se utilizaron VLANs para segmentar la red en diferentes áreas:

* VLAN 300 → Estudiantes
* VLAN 500 → Académicos
* VLAN 999 → Administrativa (nativa)

Esto permitió mejorar la organización, seguridad y eficiencia del tráfico en la red.

---

### 🔹 Inter-VLAN Routing (Router-on-a-Stick)

Se configuró en los routers R1 y R4 mediante subinterfaces:

* Permite la comunicación entre diferentes VLANs.
* Cada subinterfaz representa una VLAN específica.
* Se utilizó encapsulación **802.1Q**.

---

### 🔹 HSRP (Hot Standby Router Protocol)

Se implementó HSRP para garantizar alta disponibilidad:

* R4 actúa como **router activo**.
* R1 actúa como **router en espera (standby)**.
* Se configuraron prioridades y preempt.
* Se utilizó una IP virtual como gateway para los hosts.

Esto asegura continuidad del servicio en caso de falla de un router.

---

### 🔹 DHCP (Dynamic Host Configuration Protocol)

Configurado en R2:

* Asigna direcciones IP automáticamente a los dispositivos.
* Se crearon pools para cada VLAN.
* Se excluyeron direcciones reservadas.

También se utilizó **ip helper-address** en los routers para reenviar solicitudes DHCP.

---

### 🔹 Enrutamiento Estático

Se configuraron rutas estáticas entre routers:

* Permite la comunicación entre redes remotas.
* Se establecieron rutas hacia todas las VLANs y redes LAN.
* Se implementaron rutas por defecto.

---

### 🔹 STP (Spanning Tree Protocol)

Configurado en los switches:

* Evita bucles en la red.
* SW1 se configuró como **root bridge**.
* Mejora la estabilidad de la red.

---

### 🔹 EtherChannel (LACP)

Se implementó un canal lógico entre SW1 y SW2:

* Utiliza el protocolo **LACP**.
* Mejora el ancho de banda.
* Proporciona redundancia.

---

### 🔹 Trunking

Configurado entre switches y routers:

* Permite transportar múltiples VLANs por un solo enlace.
* Se definió VLAN nativa (999).
* Se controlaron VLANs permitidas.

---

### 🔹 DNS (Domain Name System)

Configurado en el servidor:

* Traduce nombres de dominio a direcciones IP.
* Se crearon registros para servicios internos.

---

### 🔹 Red Inalámbrica (WLAN + WLC)

Se configuró un controlador inalámbrico (WLC):

* Creación de múltiples SSIDs.
* Asociación de Access Points.
* Seguridad WPA2.
* Integración con servidor AAA.

---

### 🔹 AAA (Authentication, Authorization and Accounting)

Implementado para autenticación:

* Uso de servidor RADIUS.
* Control de acceso a la red inalámbrica.
* Gestión de usuarios.

---

### 🔹 SSH (Secure Shell)

Configurado en todos los dispositivos:

* Permite acceso remoto seguro.
* Uso de autenticación local.
* Encriptación de credenciales.

---

## 🧠 Conclusión

Este proyecto permitió integrar múltiples conceptos fundamentales de redes en un entorno práctico, reforzando habilidades en configuración, resolución de problemas y diseño de infraestructuras de red.

Se logró una red funcional con redundancia, segmentación y servicios activos, cumpliendo con los objetivos planteados y simulando un entorno real de trabajo en el área de redes y ciberseguridad.

---

## 📁 Contenido del Repositorio

* Configuraciones de routers (R1, R2, R3, R4)
* Configuraciones de switches (SW1, SW2, SW3)
* Documentación de la red
* Archivos de comandos en formato `.txt`

---

