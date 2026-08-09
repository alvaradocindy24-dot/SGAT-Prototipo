# 🛠️ Manual Técnico — SGAT

## 1. Arquitectura propuesta

El SGAT se implementa como una aplicación web de tres capas: presentación, lógica de negocio y datos.

- **Capa de presentación:** interfaz web accesible desde navegadores modernos, orientada a técnicos y administradores.
- **Capa de lógica de negocio:** servicios que implementan las reglas del sistema (registro de activos, asignaciones, mantenimientos, garantías, reportes, autenticación, control por roles y bitácora).
- **Capa de datos:** base de datos relacional que almacena activos, usuarios, asignaciones, mantenimientos, garantías y bitácora, con copias de seguridad periódicas.

## 2. Modelo entidad-relación

Entidades principales: `Activo`, `Usuario`, `AsignacionActivo`, `Mantenimiento`, `Garantia`, `Bitacora`, `Rol` y `UsuarioRol` (para RBAC).

- `Activo` 1–N `AsignacionActivo`
- `Activo` 1–N `Mantenimiento`
- `Activo` 1–N `Garantia`
- `Usuario` 1–N `AsignacionActivo`
- `Usuario` N–M `Rol` (a través de `UsuarioRol`)
- `Bitacora` referencia genérica a `Usuario` y a la entidad auditada mediante `tipoEntidad` e `idEntidad`.

## 3. Diagrama de clases

Clases de entidad: `Activo`, `Usuario`, `AsignacionActivo`, `Mantenimiento`, `Garantia`, `Rol`, `UsuarioRol`, `Bitacora`.

Clases de servicio: `ActivoService`, `AsignacionService`, `MantenimientoService`, `GarantiaService`, `ReporteService`, `AutenticacionService`, `BitacoraService`.

Controladores: `ActivoController`, `AsignacionController`, `MantenimientoController`, `GarantiaController`, `ReporteController`, `AuthController`.

## 4. Casos de uso principales (diagramas de secuencia)

- **CU-01 Registrar activo:** InterfazWeb → ActivoController → ActivoService → ActivoRepository → BitacoraService.
- **CU-02 Asignar activo:** InterfazWeb → AsignacionController → AsignacionService → ActivoService → BitacoraService.
- **CU-03 Registrar mantenimiento:** InterfazWeb → MantenimientoController → MantenimientoService → BitacoraService.
- **CU-04 Gestionar garantías:** InterfazWeb → GarantiaController → GarantiaService → BitacoraService.
- **CU-05 Consultar y generar reportes:** InterfazWeb → ReporteController → ReporteService → Repositorios (Activo, Asignacion, Mantenimiento, Garantia).
- **CU-06 Autenticarse:** InterfazWeb → AuthController → AutenticacionService → UsuarioRepository → UsuarioRolRepository.

## 5. Tecnologías utilizadas

- Frontend: HTML, CSS, JavaScript (prototipo navegable).
- Backend sugerido: JavaScript/Node o Python.
- Base de datos: relacional (por definir según implementación final).
- Control de versiones: Git / GitHub.

## 6. Estimación del proyecto

- Tamaño estimado: ~110 puntos de función no ajustados (~6.6 KLOC).
- Esfuerzo (COCOMO II, modo orgánico): ~17 persona-mes.
- Tiempo de desarrollo estimado: 7 a 8 meses calendario.

## 7. Requisitos no funcionales

- Seguridad mediante credenciales y control por roles.
- Trazabilidad de cambios mediante bitácora.
- Copias de seguridad periódicas y capacidad de crecimiento del sistema.
- Tiempos de respuesta adecuados para consultas y generación de reportes.
