---
id: introduccion
title: Introducción y Descripción
sidebar_position: 1
---

# 1. Introducción
### 1.1 Propósito
El propósito de este documento es definir las especificaciones técnicas y funcionales para la aplicación móvil **Focus Knight**. Este SRS servirá como guía para el desarrollo de la app utilizando **JavaFX Mobile** y garantizará que el producto funcione de manera óptima en dispositivos Android/iOS.

### 1.2 Alcance del Sistema
El sistema será una aplicación móvil orientada a la productividad. Permitirá a los usuarios iniciar sesiones de enfoque de 25 minutos. El principal diferenciador es su mecánica de juego inactivo (idle): la app recompensa al usuario con moneda virtual por mantener la concentración, pero aplicará un "castigo" (pérdida de monedas) si el usuario abandona la aplicación.

---

# 2. Descripción General
### 2.1 Perspectiva del Producto
Focus Knight es una aplicación móvil nativa e independiente. No requiere conexión obligatoria a internet ni backend complejo, ya que el estado del juego, el inventario y las monedas se guardarán localmente en el dispositivo del usuario.

### 2.2 Funciones del Producto
* **Gestión de Tiempo Móvil:** Temporizadores de trabajo y descanso.
* **Mecanismo Anti-Distracción:** Detección de salida de la app para aplicar castigos en el juego.
* **Economía Inactiva y Tienda:** Generación de recursos para mejorar un personaje virtual mediante controles táctiles.