---
id: requisitos
title: Requisitos e Historias
sidebar_position: 2
---

# 3. Requisitos Específicos

### 3.1 Requisitos Funcionales (RF)
| ID | Nombre | Descripción | Prioridad |
|:---|:---|:---|:---:|
| **RF-01** | Inicio de Sesión Focus | La app DEBE permitir iniciar un temporizador de 25 minutos. | Alta |
| **RF-02** | Castigo por Minimizar | La app DEBE detectar si pasa a segundo plano y cancelar la sesión. | Alta |
| **RF-03** | Generación Pasiva | La app DEBE otorgar monedas visualmente mientras esté en primer plano. | Media |
| **RF-04** | Almacenamiento Local | La app DEBE guardar el estado del jugador utilizando preferencias del sistema. | Alta |

### 3.2 Requisitos No Funcionales (RNF)
| ID | Atributo | Requisito de Calidad |
|:---|:---|:---|
| **RNF-01** | Eficiencia de Batería | Las animaciones DEBEN optimizarse para no drenar la batería. |
| **RNF-02** | Usabilidad Táctil | Los botones DEBEN tener un tamaño mínimo de `48x48 dp`. |

---

### 3.3 Historias de Usuario y Criterios de Aceptación

#### HU-01: Iniciar Sesión de Enfoque (Ref. RF-01)
**Descripción:** Como jugador, quiero iniciar un temporizador de 25 minutos para poder empezar mi sesión de concentración.
**Criterios de Aceptación:**
* La pantalla principal debe mostrar un reloj en formato `MM:SS`.
* Debe existir un botón "Iniciar" que comience la cuenta regresiva.
* El tiempo no puede ser modificado manualmente.

#### HU-02: Castigo por Distracción (Ref. RF-02)
**Descripción:** Como jugador, quiero perder el progreso de mi sesión actual si salgo de la aplicación.
**Criterios de Aceptación:**
* El sistema debe detectar cuando la aplicación pasa a segundo plano (onPause/background).
* Si pasa a segundo plano, el temporizador debe detenerse y reiniciarse a `25:00`, y las monedas de la sesión se reducen a cero.

#### HU-03: Generación de Monedas (Ref. RF-03)
**Descripción:** Como jugador, quiero ganar monedas automáticamente mientras estoy concentrado para poder comprar mejoras después.
**Criterios de Aceptación:**
* El jugador debe recibir 10 monedas virtuales por cada minuto completado en el temporizador.
* El contador de monedas de la sesión debe actualizarse visualmente en la pantalla cada vez que se gane una moneda.

#### HU-04: Guardado de Progreso (Ref. RF-04)
**Descripción:** Como jugador, quiero que mis monedas totales se guarden automáticamente para no perder mi riqueza cuando cierre la aplicación correctamente.
**Criterios de Aceptación:**
* El balance total de monedas debe guardarse en el almacenamiento local del dispositivo.
* Al abrir la aplicación (arranque en frío), el sistema debe cargar y mostrar el balance total de monedas guardado anteriormente.