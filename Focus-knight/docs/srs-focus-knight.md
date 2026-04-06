---
id: srs-focus-knight
title: Especificación de Requisitos (SRS)
sidebar_position: 1
---

# 📄 Especificación de Requisitos de Software (SRS)
**Proyecto:** Focus Knight (Pomodoro & Idle Game)  
**Versión:** 1.0.0  
**Estado:** Documento Base  
**Estándar:** ISO 29148 / IEEE 830  

---

## 1. Introducción
### 1.1 Propósito
El propósito de este documento es definir las especificaciones técnicas y funcionales para el sistema **Focus Knight**. Este SRS servirá como guía técnica para el desarrollo del juego en Java (LibGDX) y garantizará que las mecánicas cumplan con el objetivo de gestión de tiempo.

### 1.2 Alcance del Sistema
El sistema permitirá a los usuarios iniciar sesiones de enfoque (tipo Pomodoro) de 25 minutos. Durante este tiempo, un juego inactivo (idle) recompensará al usuario con moneda virtual, la cual se perderá si el temporizador es interrumpido. La moneda se podrá gastar en una tienda durante los tiempos de descanso.

---

## 2. Descripción General
### 2.1 Perspectiva del Producto
Focus Knight es una aplicación web compilada desde Java (mediante HTML5/WebGL) que se ejecutará directamente en el navegador del usuario. No requiere backend complejo, ya que el estado del juego se guardará localmente.

### 2.2 Funciones del Producto
* **Gestión de Tiempo:** Temporizadores precisos para fases de trabajo (25 min) y descanso (5 min).
* **Mecánica de Castigo/Recompensa:** Asignación de monedas por tiempo completado y pérdida total del progreso de la sesión por interrupción.
* **Tienda Virtual:** Interfaz interactiva disponible solo en tiempo de descanso para mejorar al personaje.

---

## 3. Requisitos Específicos

### 3.1 Requisitos Funcionales (RF)
| ID | Nombre | Descripción | Prioridad |
|:---|:---|:---|:---:|
| **RF-01** | Inicio de Sesión Focus | El sistema DEBE permitir al usuario iniciar un temporizador de 25 minutos sin interrupciones. | Alta |
| **RF-02** | Castigo por Interrupción | El sistema DEBE eliminar las monedas acumuladas en la sesión actual si el usuario detiene el temporizador antes de llegar a cero. | Alta |
| **RF-03** | Generación Pasiva | El sistema DEBE generar X cantidad de monedas virtuales de forma automática mientras el temporizador "Focus" esté activo. | Media |
| **RF-04** | Guardado Local | El sistema DEBE guardar el inventario y las monedas del jugador en el almacenamiento local del navegador (`localStorage`). | Alta |

### 3.2 Requisitos No Funcionales (RNF)
| ID | Atributo | Requisito de Calidad |
|:---|:---|:---|
| **RNF-01** | Rendimiento | El juego DEBE mantener una tasa de refresco constante (60 FPS) en el navegador sin consumir exceso de CPU. |
| **RNF-02** | Persistencia | Los datos guardados DEBEN estructurarse en formato JSON. |
| **RNF-03** | Compatibilidad | El juego DEBE ser jugable en navegadores modernos (Chrome, Firefox, Edge, Safari). |

---

## 4. Modelado Lógico (Diagramas Mermaid)

*(Espacio reservado para diagramas de flujo y arquitectura - En desarrollo)*

---

## 5. Matriz de Trazabilidad de Requisitos (RTM)

*(Espacio reservado para la matriz de trazabilidad - En desarrollo)*

---

## 6. Gestión de Cambios (Control de Versiones)

*(Espacio reservado para el registro de versiones - En desarrollo)*