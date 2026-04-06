---
id: casos-gherkin
title: Casos de Prueba (Gherkin)
sidebar_position: 1
---

# 🧪 Casos de Prueba

Este documento detalla los escenarios de prueba para validar los Criterios de Aceptación de las Historias de Usuario, utilizando la sintaxis Gherkin (Dado-Cuando-Entonces).

---

## HU-01: Iniciar Sesión de Enfoque

### **CP-001: Inicio exitoso del temporizador**
**Propósito:** Validar que el botón "Iniciar" comienza la cuenta regresiva correctamente.
* **Dado** que el usuario se encuentra en la pantalla principal de la aplicación.
* **Y** el temporizador marca `25:00`.
* **Cuando** el usuario presiona el botón "Iniciar".
* **Entonces** el temporizador debe cambiar a `24:59` después de un segundo.
* **Y** el botón "Iniciar" debe ocultarse de la pantalla.

### **CP-002: Inmutabilidad del tiempo**
**Propósito:** Garantizar que el usuario no pueda hacer trampa modificando el tiempo.
* **Dado** que el usuario se encuentra en la pantalla principal.
* **Cuando** el usuario intenta tocar o escribir sobre los números del reloj `25:00`.
* **Entonces** el sistema no debe abrir el teclado ni permitir la edición del texto.

---

## HU-02: Castigo por Distracción

### **CP-003: Penalización al pasar a segundo plano**
**Propósito:** Verificar que el sistema castiga al usuario si sale de la app durante una sesión activa.
* **Dado** que el usuario tiene un temporizador activo corriendo (ej. en `15:30`).
* **Y** el usuario ha recolectado `50` monedas en la sesión actual.
* **Cuando** el usuario minimiza la aplicación Focus Knight para abrir otra app (onPause).
* **Entonces** el temporizador debe detenerse y volver a `25:00`.
* **Y** las monedas de la sesión actual deben reducirse a `0`.
* **Y** al volver a abrir la app, debe mostrarse la notificación: "Tu caballero ha huido. Concéntrate."

---

## HU-03: Generación de Monedas

### **CP-004: Asignación de monedas por minuto completado**
**Propósito:** Validar que el sistema recompense al jugador con la cantidad correcta de monedas al transcurrir el tiempo.
* **Dado** que el usuario tiene un temporizador activo.
* **Y** el contador de monedas de la sesión actual muestra `0`.
* **Cuando** el temporizador descuenta exactamente un minuto (ej. pasa de `25:00` a `24:00`).
* **Entonces** el sistema debe otorgar `10` monedas virtuales.
* **Y** el contador visual en la pantalla debe actualizarse automáticamente para mostrar `10`.

---

## HU-04: Guardado de Progreso

### **CP-005: Guardado exitoso al cerrar la aplicación**
**Propósito:** Asegurar que la riqueza acumulada del jugador se persista en la memoria del teléfono.
* **Dado** que el usuario ha finalizado una sesión y su balance total es de `150` monedas.
* **Cuando** el usuario cierra la aplicación de forma normal.
* **Entonces** el sistema debe guardar el valor `150` en el almacenamiento local (Preferencias/SQLite) del dispositivo.

### **CP-006: Recuperación del progreso al inicio (Arranque en frío)**
**Propósito:** Verificar que el jugador recupere sus monedas al volver a jugar horas o días después.
* **Dado** que el almacenamiento local del dispositivo tiene registrado un balance de `150` monedas.
* **Cuando** el usuario abre la aplicación de Focus Knight desde cero (arranque en frío).
* **Entonces** la pantalla principal debe cargar el dato.
* **Y** el balance total de monedas visible debe mostrar `150`.