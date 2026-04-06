---
id: plan-sprint-1
title: Sprint 1 - El Bucle Central
sidebar_position: 1
---

# 🏃‍♂️ Planificación: Sprint 1 (MVP)

**Nombre del Sprint:** El Bucle Central  
**Objetivo del Sprint:** Construir el Producto Mínimo Viable (MVP). El jugador debe poder iniciar un cronómetro funcional, generar monedas mientras la app esté abierta, y ser castigado perdiendo el progreso si la aplicación pasa a segundo plano.

---

## 📦 Sprint Backlog (Historias Incluidas)

Las siguientes Historias de Usuario (HU) han sido seleccionadas para este Sprint por ser críticas para el funcionamiento básico de la aplicación.

### 1. HU-01: Iniciar Sesión de Enfoque
* **Prioridad:** Crítica ⭐⭐⭐
* **Dependencias:** Ninguna.
* **Criterios de Aceptación a cumplir:** Mostrar reloj `25:00`, botón de "Iniciar" funcional, cuenta regresiva segundo a segundo, bloqueo de edición manual.

### 2. HU-02: Castigo por Distracción
* **Prioridad:** Alta ⭐⭐⭐
* **Dependencias:** Requiere que HU-01 esté terminada.
* **Criterios de Aceptación a cumplir:** Detección de paso a segundo plano (background), reinicio del cronómetro, reseteo de monedas a `0`, alerta de castigo al volver.

### 3. HU-03: Generación de Monedas
* **Prioridad:** Media ⭐⭐
* **Dependencias:** Requiere que HU-01 esté terminada.
* **Criterios de Aceptación a cumplir:** Otorgar 10 monedas por minuto completado, actualización de la UI en tiempo real.

---

## 🧊 Product Backlog (Postergado para Sprint 2+)

Las siguientes historias fueron analizadas pero **excluidas** de este Sprint para mantener el foco en el flujo principal (MVP).

* **HU-04 (Guardado Local):** Se pospone. Motivo: La persistencia de datos no aporta valor hasta que la generación y pérdida de monedas (HU-02 y HU-03) sean 100% estables en memoria volátil.
* **Diseño de Tienda de Ítems:** Se pospone. Requiere arte (sprites) y una economía balanceada.

---

## 🛠️ Desglose de Tareas Técnicas y Estimación

*(Esta sección se llenará con las tareas de desarrollo específicas (UI, Lógica JavaFX, etc.) y sus respectivos Puntos de Historia).*