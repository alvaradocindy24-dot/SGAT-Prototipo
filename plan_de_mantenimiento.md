# 🔧 Plan de Mantenimiento — SGAT

## 1. Objetivo

Establecer las actividades necesarias para asegurar la disponibilidad, corrección de errores y evolución del Sistema de Gestión de Activos Tecnológicos (SGAT) una vez puesto en producción.

## 2. Tipos de mantenimiento

- **Correctivo:** solución de errores detectados en el funcionamiento del sistema (bugs, fallos de validación, errores de cálculo en reportes).
- **Preventivo:** revisiones periódicas de la base de datos, respaldo de información y monitoreo de rendimiento.
- **Adaptativo:** ajustes ante cambios en el entorno tecnológico (actualizaciones de navegadores, dependencias o infraestructura).
- **Evolutivo:** incorporación de nuevas funcionalidades solicitadas por los usuarios (por ejemplo, nuevos tipos de reportes o roles).

## 3. Actividades periódicas

| Actividad | Frecuencia | Responsable |
|---|---|---|
| Respaldo de base de datos | Semanal | Administrador del sistema |
| Revisión de bitácora de errores | Semanal | Equipo técnico |
| Actualización de dependencias | Mensual | Equipo de desarrollo |
| Revisión de garantías próximas a vencer | Mensual | Administrador de activos |
| Auditoría de accesos y roles | Trimestral | Administrador del sistema |

## 4. Procedimiento ante incidentes

1. Registrar el incidente en la bitácora del sistema.
2. Clasificar la severidad (crítica, alta, media, baja).
3. Asignar el incidente al responsable correspondiente.
4. Aplicar la corrección en un ambiente de pruebas antes de desplegar a producción.
5. Documentar la solución aplicada y cerrar el incidente.

## 5. Control de versiones para mantenimiento

Todo cambio de mantenimiento se gestiona mediante Git, utilizando ramas específicas y commits con el prefijo `fix:` para correcciones o `chore:` para tareas de mantenimiento técnico del repositorio.
