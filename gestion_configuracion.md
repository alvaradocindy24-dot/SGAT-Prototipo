# ⚙️ Plan de Gestión de Configuración — SGAT

## 1. Objetivo

Definir los lineamientos para el control de versiones, la gestión de cambios y el resguardo de los artefactos del proyecto SGAT durante su ciclo de vida.

## 2. Herramienta de control de versiones

Se utiliza **Git** junto con un repositorio remoto en **GitHub** para el control de versiones del código fuente y la documentación del proyecto.

## 3. Estructura de ramas

- `main`: rama estable con las versiones entregables del prototipo y la documentación.
- Ramas de trabajo (feature/fix): utilizadas para desarrollar cambios específicos antes de integrarlos a `main`.

## 4. Convención de commits

| Prefijo | Uso |
|---|---|
| `feat:` | Nuevas funcionalidades |
| `fix:` | Corrección de errores |
| `docs:` | Cambios en documentación |
| `test:` | Evidencias y casos de prueba |
| `chore:` | Tareas de mantenimiento del repositorio |

## 5. Elementos de configuración controlados

- Prototipo navegable (`sgat-prototipo.html`).
- Documentación técnica y de usuario (`manual_usuario.md`, `manual_tecnico.md`).
- Evidencias de pruebas (`evidencias_pruebas.md`).
- Planes de mantenimiento y configuración (`plan_de_mantenimiento.md`, `gestion_configuracion.md`).
- Conclusiones y recomendaciones (`conclusiones_recomendaciones.md`).

## 6. Gestión de versiones (releases)

Cada entrega significativa del proyecto se etiqueta mediante un **tag de versión** (por ejemplo, `v1.0.0`), acompañado de notas de la entrega que describen los avances incorporados.

## 7. Respaldo y trazabilidad

El historial de commits, ramas y releases en GitHub constituye la evidencia principal de trazabilidad del proyecto, permitiendo identificar qué cambios se realizaron, cuándo y por qué motivo.
