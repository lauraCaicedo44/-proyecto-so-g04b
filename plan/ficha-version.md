# Ficha de versión - Grupo 04B

## 1. Debian (VM gráfica: `g04b-grafica`)

| Pregunta | Respuesta | Enlace de verificación |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Debian 12 "Bookworm" (o Debian 13 "Trixie" estable vigente; verificar en sitio oficial al descargar ISO) | https://www.debian.org/releases/ |
| Hasta cuándo recibe actualizaciones de seguridad | Soporte estándar de 3 años + soporte LTS hasta 5 años desde su lanzamiento | https://www.debian.org/security/ |
| Requisitos de hardware y funcionamiento en VirtualBox | Mínimo 2 GB de RAM (2 a 4 GB recomendados para entorno gráfico), 25 GB de disco y 2 CPU en VirtualBox 7.x | https://www.debian.org/releases/stable/amd64/ch03s04.es.html |
| Particionado manual en el instalador | Sí, mediante el instalador gráfico/texto en la opción «Manual» (permite crear `/`, `swap` y `/home`) | https://www.debian.org/doc/ |
| Guía oficial para instalar Docker Engine en la familia | Sí, Docker ofrece repositorio oficial para Debian (`apt`) | https://docs.docker.com/engine/install/debian/ |
| Imagen base del Dockerfile para esta versión | No aplica como imagen base del grupo (asignada a VM gráfica), pero cuenta con imagen oficial en Docker Hub | https://hub.docker.com/_/debian |

## 2. AlmaLinux (VM de consola: `g04b-consola`)

| Pregunta | Respuesta | Enlace de verificación |
|---|---|---|
| Versión elegida y fecha de lanzamiento | AlmaLinux OS 9.x (compatible binariamente con RHEL 9) | https://wiki.almalinux.org/release-notes/ |
| Hasta cuándo recibe actualizaciones de seguridad | Soporte activo hasta mayo de 2027 y soporte de seguridad hasta mayo de 2032 | https://wiki.almalinux.org/FAQ.html |
| Requisitos de hardware y funcionamiento en VirtualBox | 2 GB de RAM en Sprint 1-2 (3 GB en Sprint 3 para Minikube), 25 GB de disco (`/`, `swap`, `/home`, `/var` de 10 GB) y 2 CPU | https://wiki.almalinux.org/documentation/installation-guide.html |
| Particionado manual en el instalador | Sí, el instalador Anaconda permite almacenamiento personalizado («Custom») | https://wiki.almalinux.org/documentation/installation-guide.html |
| Guía oficial para instalar Docker Engine en la familia | Sí, mediante el procedimiento oficial de Docker para familia RHEL/CentOS (`dnf`) | https://docs.docker.com/engine/install/centos/ |
| Imagen base del Dockerfile para esta versión | No aplica como imagen base del grupo (asignada a VM de consola), cuenta con imagen oficial en Docker Hub | https://hub.docker.com/_/almalinux |

## 3. Rocky Linux (Imagen base del Dockerfile)

| Pregunta | Respuesta | Enlace de verificación |
|---|---|---|
| Versión elegida y fecha de lanzamiento | `rockylinux:9` (imagen oficial de Rocky Linux 9 para contenedores) | https://hub.docker.com/_/rockylinux |
| Hasta cuándo recibe actualizaciones de seguridad | Ciclo de vida alineado con RHEL 9 (soporte de seguridad hasta mayo de 2032) | https://docs.rockylinux.org/ |
| Requisitos de hardware y funcionamiento en VirtualBox | Se ejecuta como contenedor sobre Docker Engine dentro de la VM `g04b-consola` | https://docs.docker.com/engine/install/ |
| Particionado manual en el instalador | No aplica (es una imagen base de contenedor, no una instalación de VM) | https://hub.docker.com/_/rockylinux |
| Guía oficial para instalar Docker Engine en la familia | Procedimiento oficial de Docker para familia RHEL/CentOS (`dnf`); dentro del contenedor se usa `dnf` para instalar `git`, `curl`, editor y compilador | https://docs.docker.com/engine/install/centos/ |
| Imagen base del Dockerfile para esta versión | Sí, disponible oficialmente en Docker Hub bajo el tag `rockylinux:9` | https://hub.docker.com/_/rockylinux |
