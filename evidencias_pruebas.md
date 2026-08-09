# 🧪 Evidencias de Pruebas — SGAT

## 1. Objetivo

Documentar los casos de prueba ejecutados sobre el prototipo navegable del SGAT, cubriendo los principales casos de uso definidos en la ingeniería de requerimientos.

## 2. Casos de prueba

| ID | Caso de uso | Escenario | Resultado esperado | Resultado obtenido | Estado |
|---|---|---|---|---|---|
| CP-01 | CU-01 Registrar activo | Completar formulario con datos válidos | El activo se registra y aparece en el inventario | Activo registrado correctamente | ✅ Aprobado |
| CP-02 | CU-01 Registrar activo | Enviar formulario con número de serie duplicado | El sistema rechaza el registro | Mensaje de error mostrado | ✅ Aprobado |
| CP-03 | CU-02 Asignar activo | Asignar activo disponible a un usuario | El activo cambia a estado "Asignado" | Estado actualizado correctamente | ✅ Aprobado |
| CP-04 | CU-03 Registrar mantenimiento | Registrar mantenimiento preventivo | El mantenimiento aparece en el historial del activo | Registro visible en historial | ✅ Aprobado |
| CP-05 | CU-04 Gestionar garantías | Registrar nueva garantía con fecha de vencimiento próxima | Se genera alerta de garantía por vencer | Alerta generada correctamente | ✅ Aprobado |
| CP-06 | CU-05 Generar reportes | Filtrar reporte de inventario por ubicación | Se muestra listado filtrado | Listado correcto | ✅ Aprobado |
| CP-07 | CU-06 Autenticarse | Ingresar credenciales incorrectas | Se muestra mensaje de error y se permite reintentar | Mensaje mostrado correctamente | ✅ Aprobado |
| CP-08 | CU-06 Autenticarse | Ingresar credenciales válidas | Redirección al panel principal según el rol | Redirección exitosa | ✅ Aprobado |

## 3. Evidencia visual

Las capturas de pantalla del prototipo navegable (panel principal, formularios, listados y alertas) se encuentran adjuntas en la carpeta de evidencias del curso y en el historial de commits del repositorio.

## 4. Trazabilidad

Cada caso de prueba se relaciona con su requerimiento funcional (RF) y caso de uso (CU) correspondiente, permitiendo verificar la cobertura de las pruebas frente a los requerimientos definidos en el proyecto.

## 5. Conclusión de las pruebas

Los casos de prueba ejecutados confirman que las funcionalidades principales del prototipo (registro de activos, asignaciones, mantenimientos, garantías, reportes y autenticación) operan conforme a lo esperado en el entorno de prototipo visual.
