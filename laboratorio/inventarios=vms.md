# Inventario de máquinas virtuales

## 1. Descripción

Este documento contiene el inventario de máquinas virtuales utilizadas en el laboratorio de ciberseguridad.

Su propósito es mantener un registro de los sistemas operativos, recursos asignados, configuraciones de red y funciones de cada máquina virtual, facilitando la administración del entorno y la reproducción de las prácticas.

**Hipervisor:** Oracle VirtualBox  
**Sistema anfitrión:** Debian 12  
**Última actualización:** 2026-10-25

## 2. Inventario general

| ID | Nombre | Sistema operativo | Función | Estado |
|---|---|---|---|---|
| VM-01 | DebServ | Debian 12 | Servidor debian como objetivo de monitoreo y hardening | En configuración |
| VM-02 | Windows 11 | Windows 11 | Sistema cliente de pruebas | Pendiente |
| VM-03 | Windows Server | Windows Server | Servicios y administración de red | Pendiente |

> Los estados deben actualizarse conforme se instalen y configuren las máquinas virtuales.

## 3. Recursos asignados

| ID | RAM | CPU (vCPU) | Disco virtual | Formato |
|---|---|---|---|---|
| VM-01 | 4 GB  | 2 vCPU | 20 GB. | VDI/VMDK |
| VM-02 | Por definir | Por definir | Por definir | VDI/VMDK |
| VM-03 | Por definir | Por definir | Por definir | VDI/VMDK |

## 4. Configuración de red

| ID | Adaptador 1 | Adaptador 2 | IP Host-only |
|---|---|---|---|
| VM-01 | NAT | Host-only | Por asignar |
| VM-02 | NAT | Host-only | Por asignar |
| VM-03 | NAT | Host-only | Por asignar |

### Red del laboratorio

| Parámetro | Configuración prevista |
|---|---|
| Tipo de red | Host-only |
| Interfaz del anfitrión | vboxnet0 |
| Red IPv4 | 192.168.56.0/24 |
| IP del anfitrión | 192.168.56.1 |
| DHCP | Por definir |

Esta red permitirá la comunicación entre el sistema anfitrión y las máquinas virtuales conectadas al mismo segmento Host-only.

La configuración definitiva se registrará después de verificar las interfaces de VirtualBox.

## 5. Funciones de las máquinas virtuales

### VM-01: Kali Linux

**Objetivo:** Utilizar herramientas de análisis de tráfico, reconocimiento y evaluación de seguridad en entornos autorizados y controlados.

**Herramientas previstas:**
- Wireshark
- tcpdump
- Nmap

### VM-02: Windows 11

**Objetivo:** Disponer de un sistema cliente para generar tráfico de red, analizar eventos y realizar prácticas de configuración y seguridad.

### VM-03: Windows Server

**Objetivo:** Implementar servicios de red y practicar tareas de administración, configuración y monitoreo de infraestructura.

## 6. Consideraciones de seguridad

- Las prácticas se realizarán en un entorno controlado.
- Se evitará exponer servicios vulnerables a redes externas.
- Las direcciones IP documentadas corresponderán a la red privada del laboratorio.
- Se utilizarán instantáneas antes de realizar modificaciones importantes.
- No se almacenarán contraseñas, credenciales ni información sensible en el repositorio.

## 7. Registro de cambios

| Fecha | Máquina virtual | Modificación |
|---|---|---|
| AAAA-MM-DD | VM-01 | Creación del registro inicial |
