# Iron & Citrus

## 1. Descripción

Iron & Citrus es una plataforma web orientada a ejercicio, nutrición y bienestar.
El proyecto contempla tres ejes principales:

* **Alimentos y productos**: consulta de información nutricional, registro de productos, comparación nutricional e información verificable.
* **Planes personalizados**: generación de planes nutricionales y rutinas de ejercicio adaptados a los objetivos del usuario.
* **Comunidad**: foro, publicaciones, comentarios y validación de información por usuarios con permisos.

Actores definidos: **Usuario**, **Validador** y **Administrador**.

## 2. Estado actual del proyecto

**Fase HTML estático — completada**

Actualmente se ha construido únicamente la estructura HTML semántica de la interfaz (22 páginas). Existe navegación entre páginas mediante enlaces relativos, pero **no existe lógica funcional alguna**.

Actualmente **NO están implementados**:

* CSS
* JavaScript
* React
* Tailwind
* Backend
* API
* Base de datos
* Autenticación real
* Persistencia de datos
* Generación real mediante IA

## 3. Tecnologías

### Implementadas actualmente

* HTML5 (HTML semántico puro)

### Previstas para fases posteriores

* CSS
* JavaScript
* React.js
* Tailwind CSS
* Node.js / Express
* PostgreSQL
* Integración con IA

> Las tecnologías previstas **todavía no forman parte** de la implementación actual. No se ha instalado ninguna dependencia.

## 4. Estructura del proyecto

Estructura real actual:

```
index.html

pages/
├── auth/
│   ├── login.html
│   ├── register.html
│   └── register-business.html
├── foods/
│   ├── index.html
│   ├── detail.html
│   ├── compare.html
│   ├── register.html
│   └── edit.html
├── plans/
│   ├── index.html
│   ├── nutrition.html
│   ├── exercise.html
│   └── generate.html
├── community/
│   ├── forum.html
│   ├── post.html
│   └── create-post.html
├── admin/
│   ├── dashboard.html
│   ├── users.html
│   ├── foods.html
│   ├── validations.html
│   └── reports.html
└── profile.html
```

Finalidad de cada módulo:

* **`pages/auth/`** — autenticación: inicio de sesión, registro de usuario y registro de empresa.
* **`pages/foods/`** — alimentos y productos: consulta, ficha nutricional, comparación, registro y edición.
* **`pages/plans/`** — planes personalizados: listado, plan nutricional, rutina de ejercicio y formulario de generación.
* **`pages/community/`** — comunidad: foro, publicación con comentarios y creación de publicaciones.
* **`pages/admin/`** — administración: panel general, usuarios, alimentos, validaciones y reportes.
* **`pages/profile.html`** — perfil de usuario: datos, edición y actividad.

## 5. Páginas implementadas

Las 22 páginas son documentos HTML5 completos e independientes:

### Autenticación

`login.html`, `register.html` y `register-business.html` representan el inicio de sesión, el registro de usuario y el registro de empresa.

### Alimentos y productos

`index.html` (listado y búsqueda), `detail.html` (ficha nutricional con tabla por 100 g y por porción), `compare.html` (comparación nutricional), `register.html` (registro) y `edit.html` (modificación).

### Planes

`index.html` (listado de planes), `nutrition.html` (consulta de plan nutricional con distribución de comidas y macros), `exercise.html` (consulta de rutina con distribución semanal) y `generate.html` (formulario estructural de generación).

### Comunidad

`forum.html` (foro con categorías y publicaciones), `post.html` (publicación con comentarios y estado de validación) y `create-post.html` (creación de publicaciones).

### Administración

`dashboard.html` (panel con indicadores), `users.html`, `foods.html`, `validations.html` y `reports.html`.

### Perfil

`profile.html` representa la información del perfil de usuario, la edición de datos y contraseña, y la actividad del usuario.

## 6. Funcionalidad actual

Las páginas son **actualmente estáticas**.

Los formularios, botones y enlaces representan la estructura y la navegación de la futura aplicación, pero **todavía no ejecutan operaciones reales**. No hay lógica de autenticación, permisos, persistencia ni procesamiento.

Distinción:

* **Representado en HTML** — estructura visual y navegación (formularios, botones, tablas, enlaces).
* **Funcionalidad real pendiente** — todo comportamiento requiriado backend, base de datos o JavaScript (enviar datos, validar, generar planes, gestionar usuarios, etc.).

## 7. Requisitos funcionales representados

Relación de requisitos con las páginas existentes. Ninguno está "completamente implementado" porque todavía no existe backend ni lógica:

| Requisito | Páginas relacionadas | Estado |
|---|---|---|
| **RF01 Autenticación** | `auth/login.html` | Estructuralmente representado. Funcionalidad pendiente. |
| **RF02 Registro y perfiles** | `auth/register.html`, `auth/register-business.html`, `profile.html` | Parcialmente representado: existe el registro de empresa, pero el perfil/gestión de empresa aún no tiene página. |
| **RF03 Gestión de alimentos/productos** | `foods/index.html`, `foods/detail.html`, `foods/register.html`, `foods/edit.html`, `admin/foods.html` | Parcialmente representado: consulta, detalle, registro y edición estructurados; la eliminación y la aplicación de permisos quedan pendientes. |
| **RF04 Validación comunitaria** | `community/post.html`, `admin/validations.html`, `admin/foods.html` | Estructuralmente representado: estado de validación y gestión de cola. Funcionalidad pendiente. |
| **RF05 Comparación nutricional** | `foods/compare.html` | Estructuralmente representado. Funcionalidad pendiente. |
| **RF06 Planes personalizados** | `plans/index.html`, `plans/nutrition.html`, `plans/exercise.html`, `plans/generate.html` | Estructuralmente representado. La generación real mediante IA está pendiente. |
| **RF07 Comunicación/comunidad** | `community/forum.html`, `community/post.html`, `community/create-post.html` | Parcialmente representado: foro, publicaciones y comentarios estructurados; falta el vínculo entre productos y discusiones. |
| **RF08 Seguridad** | — | Pendiente de implementación funcional: no existe autenticación real ni control de permisos. |

## 8. Auditoría técnica HTML

Resultados de la auditoría final sobre los 22 archivos:

* 22/22 archivos revisados
* 22/22 con etiquetas balanceadas
* 22/22 con jerarquía de encabezados correcta (h1 → h2 → h3)
* 22/22 con labels, inputs, IDs y botones correctamente estructurados
* 9/9 tablas con `<caption>`
* 9/9 tablas con `scope` en los encabezados
* 251 enlaces internos verificados
* 0 enlaces rotos
* sin CSS
* sin JavaScript
* sin React
* sin Tailwind
* sin backend
* sin API
* sin dependencias

> Esta auditoría valida la **estructura HTML** (sintaxis, semántica, enlaces y accesibilidad básica). No valida la funcionalidad completa de la aplicación, que aún no existe.

## 9. Contenido de ejemplo

La interfaz contiene datos estáticos utilizados únicamente para representar visualmente las páginas:

* alimentos (p. ej. avena integral, pechuga de pollo, arroz integral)
* valores nutricionales por 100 g y por porción
* planes de ejemplo (plan nutricional de 1.900 kcal, rutina de fuerza)
* publicaciones y comentarios del foro
* usuarios y validadores ficticios
* indicadores administrativos (usuarios registrados, alimentos, reportes, etc.)

Estos datos **todavía no provienen de una base de datos**; son contenido de ejemplo incrustado en el HTML.

## 10. Pendientes identificados

### Corrección inmediata

* Resolver la inconsistencia entre la "rutina de 4 días" y la tabla que actualmente muestra 3 días (`plans/exercise.html` y `plans/index.html`).

### Pendientes de desarrollo

* Comportamiento dinámico (JavaScript/React)
* Autenticación real
* Base de datos
* Backend
* API
* Generación real de planes mediante IA
* Estado de verificación en las fichas de alimentos
* Vínculo entre productos y discusiones de la comunidad
* Funcionamiento real de reportes
* Control de permisos
* Perfil/gestión de empresas
* Ajuste de planes

### Requieren definición de alcance

* Suspensión/reactivación de usuarios
* Reportes iniciados desde la interfaz pública
* Tipo de empresa en el registro empresarial

## 11. Arquitectura prevista

La arquitectura documentada del proyecto contempla una arquitectura **MVC** complementada con separación por controladores, servicios, modelos, repositorios/DAO y DTO.

La implementación tecnológica final se adaptará al stack previsto: **React** (frontend), **Node.js/Express** (backend) y **PostgreSQL** (base de datos).

No se documentan aquí implementaciones que todavía no existen; esta sección describe únicamente la dirección prevista.

## 12. Próximas fases

1. HTML — **COMPLETADO**
2. Corrección final de contenido HTML
3. CSS
4. JavaScript
5. React
6. Backend con Node.js/Express
7. PostgreSQL
8. Integración frontend/backend
9. IA para generación de planes
10. Pruebas y validación final

## 13. Reglas para continuar el desarrollo

Reglas a respetar al continuar el desarrollo con OpenCode:

* Respetar los requisitos documentados del proyecto.
* No inventar funcionalidades.
* No implementar fases futuras antes de tiempo.
* Conservar las funcionalidades existentes al modificar código.
* No eliminar información sin justificarlo.
* Separar claramente las funcionalidades implementadas de las planificadas.
* Mantener una estructura modular.
* Actualizar este README cuando cambie significativamente el estado del proyecto.
* Antes de realizar cambios grandes, analizar primero el código existente.
* Verificar enlaces y estructura después de modificaciones importantes.