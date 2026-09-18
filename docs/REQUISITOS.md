# Iron & Citrus — Requisitos del sistema

## 1. Información general

* **Nombre del proyecto**: Iron & Citrus.
* **Propósito**: plataforma web orientada al ejercicio, la nutrición y el bienestar.
* **Descripción general**: Iron & Citrus centraliza la consulta de información nutricional, la generación de planes de ejercicio y alimentación, y la participación en una comunidad con validación de información.
* **Alcance conocido**: la documentación actual del proyecto contempla los siguientes conceptos:
  * Generación de planes de ejercicio y alimentación.
  * Biblioteca de alimentos, productos y marcas.
  * Información nutricional.
  * Comunidad.
  * Publicaciones y comentarios.
  * Validación de información.

> Iron & Citrus **no es un marketplace agrícola**.

## 2. Actores del sistema

* **Usuario** — persona que se registra en la plataforma, consulta alimentos/productos, genera y consulta planes, y participa en la comunidad (publicaciones y comentarios).
* **Validador** — usuario con permisos de validación que verifica la información publicada en la plataforma (alimentos/productos y contenido comunitario).
* **Administrador** — responsable de la administración general de la plataforma: gestión de usuarios, alimentos, validaciones y reportes.

No se definen otros actores en la documentación del proyecto.

## 3. Módulos del sistema

| Módulo | Alcance | Requisito relacionado |
| --- | --- | --- |
| **Autenticación** | Inicio de sesión, registro de usuarios y registro de empresas. | RF01, RF02 |
| **Usuarios y perfiles** | Perfil de usuario, datos personales y edición; actores Usuario, Validador y Administrador. | RF02, RF08 |
| **Alimentos y productos** | Biblioteca de alimentos, productos y marcas; consulta, registro, modificación y eliminación según permisos. | RF03 |
| **Información nutricional** | Valores nutricionales por 100 g y por porción, con información verificable. | RF03, RF04 |
| **Comparación nutricional** | Comparación de información nutricional entre productos. | RF05 |
| **Planes personalizados** | Generación y consulta de planes nutricionales personalizados. | RF06 |
| **Ejercicio** | Rutinas de ejercicio personalizadas y su consulta. | RF06 |
| **Comunidad / Foro** | Foro, publicaciones, comentarios y participación de usuarios. | RF07 |
| **Validación** | Validación de información por usuarios con permisos (Validador). | RF04 |
| **Administración** | Administración general de la plataforma, gestión de usuarios y de alimentos. | RF02, RF03 |
| **Reportes** | Gestión de reportes de la plataforma. | RF08 (relacionado) |

## 4. Requisitos funcionales

### RF01 — Autenticación segura

* **Código**: RF01
* **Nombre**: Autenticación segura
* **Descripción**: inicio de sesión de los usuarios de la plataforma.
* **Actor(es) relacionado(s)**: Usuario, Validador, Administrador.
* **Estado actual**: Estructuralmente representado (página de login en HTML). La autenticación real aún no existe.

### RF02 — Registro y gestión de usuarios/empresas

* **Código**: RF02
* **Nombre**: Registro y gestión de usuarios/empresas
* **Descripción**: registro de usuarios, registro de empresas y perfil de usuario; gestión de usuarios por parte de la administración.
* **Actor(es) relacionado(s)**: Usuario, Administrador.
* **Estado actual**: Parcialmente representado. Existen el registro de usuario, el registro de empresa y el perfil de usuario; el perfil/gestión de empresa todavía no tiene página.

### RF03 — Gestión de alimentos/productos

* **Código**: RF03
* **Nombre**: Gestión de alimentos/productos
* **Descripción**: consulta de información nutricional, registro de alimentos/productos y marcas, y modificación y eliminación según los permisos.
* **Actor(es) relacionado(s)**: Usuario, Validador, Administrador.
* **Estado actual**: Parcialmente representado. Consulta, detalle, registro y edición están estructurados; la eliminación y la aplicación de permisos quedan pendientes.

### RF04 — Validación comunitaria

* **Código**: RF04
* **Nombre**: Validación comunitaria
* **Descripción**: validación de la información de alimentos/productos y contenido comunitario por usuarios con permisos de validación.
* **Actor(es) relacionado(s)**: Validador.
* **Estado actual**: Estructuralmente representado. El estado de validación y la cola de validaciones están representados; la lógica de validación no existe.

### RF05 — Comparador nutricional

* **Código**: RF05
* **Nombre**: Comparador nutricional
* **Descripción**: comparación nutricional entre productos de la biblioteca.
* **Actor(es) relacionado(s)**: Usuario.
* **Estado actual**: Estructuralmente representado. La funcionalidad real de comparación está pendiente.

### RF06 — Planes personalizados

* **Código**: RF06
* **Nombre**: Planes personalizados
* **Descripción**: generación de planes nutricionales personalizados y de rutinas de ejercicio mediante inteligencia artificial, con consulta y ajuste de los planes.
* **Actor(es) relacionado(s)**: Usuario.
* **Estado actual**: Estructuralmente representado. La generación real mediante IA y el ajuste de planes están pendientes.

### RF07 — Comunicación

* **Código**: RF07
* **Nombre**: Comunicación
* **Descripción**: comunidad mediante foro, publicaciones y comentarios, con participación de los usuarios.
* **Actor(es) relacionado(s)**: Usuario.
* **Estado actual**: Parcialmente representado. Foro, publicaciones y comentarios están estructurados; el vínculo entre productos y discusiones está pendiente.

### RF08 — Seguridad

* **Código**: RF08
* **Nombre**: Seguridad
* **Descripción**: protección del acceso a la plataforma y control de permisos de los actores (Usuario, Validador, Administrador).
* **Actor(es) relacionado(s)**: Usuario, Validador, Administrador.
* **Estado actual**: Pendiente de implementación funcional. No existe autenticación real ni control de permisos.

## 5. Requisitos no funcionales

> Ninguno de estos requisitos está implementado ni verificado funcionalmente en la fase actual (HTML estático).

| Código | Categoría | Descripción | Estado |
| --- | --- | --- | --- |
| **RNF01** | Usabilidad | La interfaz debe ser clara y navegable para el usuario | Pendiente de implementación/verificación |
| **RNF02** | Disponibilidad | Disponibilidad del servicio del **99%** | Pendiente de implementación/verificación |
| **RNF03** | Seguridad / cifrado | Cifrado de contraseñas y datos sensibles, protección del acceso | Pendiente de implementación/verificación |
| **RNF04** | Escalabilidad | Capacidad de la plataforma para crecer en usuarios, productos y datos | Pendiente de implementación/verificación |
| **RNF05** | Compatibilidad | Compatibilidad con navegadores web modernos | Pendiente de implementación/verificación |
| **RNF06** | Mantenibilidad | Arquitectura modular que permita mantener y evolucionar el sistema | Pendiente de implementación/verificación |
| **RNF07** | Rendimiento | Consultas inferiores a **2 segundos** y páginas con carga inferior a **3 segundos** | Pendiente de implementación/verificación |
| **RNF08** | Accesibilidad | HTML semántico, etiquetas asociadas a campos y jerarquía de encabezados correcta | Parcialmente atendida en la estructura HTML actual; pendiente de verificación funcional |

## 6. Reglas y decisiones de alcance

* Iron & Citrus **no es un marketplace agrícola**.
* La biblioteca contiene **alimentos, productos y marcas**.
* La plataforma incluye **información nutricional**.
* Existe una **comunidad** mediante foro, publicaciones y comentarios.
* Existe **validación de información** por usuarios con los permisos correspondientes (Validador).
* **No se debe introducir un sistema de votos** sin que esté definido como requisito.
* **No se deben inventar funcionalidades**.
* **No se deben inventar actores**.
* Los **datos estáticos** actuales son solamente datos de demostración.

## 7. Funcionalidades actualmente representadas en HTML

> "Representado" significa que existe la estructura HTML de la página, **no** que la funcionalidad esté operativa.

| Requisito | Páginas relacionadas | Representación actual |
| --- | --- | --- |
| **RF01 — Autenticación** | `pages/auth/login.html` | Formulario estructural de inicio de sesión |
| **RF02 — Registro y perfiles** | `pages/auth/register.html`, `pages/auth/register-business.html`, `pages/profile.html`, `pages/admin/users.html` | Registro de usuario, registro de empresa y perfil de usuario estructurados |
| **RF03 — Gestión de alimentos/productos** | `pages/foods/index.html`, `pages/foods/detail.html`, `pages/foods/register.html`, `pages/foods/edit.html`, `pages/admin/foods.html` | Listado, ficha, registro y edición estructurales |
| **RF04 — Validación comunitaria** | `pages/community/post.html`, `pages/admin/validations.html`, `pages/admin/foods.html` | Estado de validación y cola de validaciones estructurados |
| **RF05 — Comparación nutricional** | `pages/foods/compare.html` | Selección y tabla de comparación estructurales |
| **RF06 — Planes personalizados** | `pages/plans/index.html`, `pages/plans/nutrition.html`, `pages/plans/exercise.html`, `pages/plans/generate.html` | Listado, consulta y formulario de generación estructurales |
| **RF07 — Comunicación** | `pages/community/forum.html`, `pages/community/post.html`, `pages/community/create-post.html` | Foro, publicación, comentarios y creación estructurales |
| **RF08 — Seguridad** | Sin páginas funcionales | Solo se representa la estructura de acceso; sin lógica |

## 8. Funcionalidades pendientes

Carencias identificadas durante la auditoría. **No constituyen requisitos nuevos**; son elementos pendientes dentro del alcance actual:

* Autenticación real.
* Persistencia de datos.
* Permisos reales.
* Generación real de planes mediante IA.
* Perfil/gestión de empresa.
* Estado de verificación en fichas de alimentos.
* Vínculo entre productos y discusiones.
* Funcionamiento real de reportes.
* Ajuste de planes.
* Backend.
* API.
* Base de datos.

## 9. Elementos pendientes de definición

Puntos cuyo alcance todavía debe decidirse. **No se decide en este documento** si forman parte del sistema:

* Suspensión/reactivación de usuarios.
* Reportes iniciados desde la interfaz pública.
* Tipo de empresa en el registro empresarial.

## 10. Trazabilidad

| Requisito | Módulo | Páginas HTML actuales | Estado |
| --- | --- | --- | --- |
| **RF01** — Autenticación | Autenticación | `pages/auth/login.html` | Estructuralmente representado |
| **RF02** — Registro y perfiles | Autenticación, Usuarios y perfiles, Administración | `pages/auth/register.html`, `pages/auth/register-business.html`, `pages/profile.html`, `pages/admin/users.html` | Parcialmente representado |
| **RF03** — Gestión de alimentos/productos | Alimentos y productos, Información nutricional, Administración | `pages/foods/index.html`, `pages/foods/detail.html`, `pages/foods/register.html`, `pages/foods/edit.html`, `pages/admin/foods.html` | Parcialmente representado |
| **RF04** — Validación comunitaria | Validación, Comunidad | `pages/community/post.html`, `pages/admin/validations.html`, `pages/admin/foods.html` | Estructuralmente representado |
| **RF05** — Comparación nutricional | Comparación nutricional | `pages/foods/compare.html` | Estructuralmente representado |
| **RF06** — Planes personalizados | Planes personalizados, Ejercicio | `pages/plans/index.html`, `pages/plans/nutrition.html`, `pages/plans/exercise.html`, `pages/plans/generate.html` | Estructuralmente representado |
| **RF07** — Comunicación | Comunidad / Foro | `pages/community/forum.html`, `pages/community/post.html`, `pages/community/create-post.html` | Parcialmente representado |
| **RF08** — Seguridad | Autenticación, Administración | Sin páginas funcionales | Pendiente de implementación funcional |

## 11. Restricciones para el desarrollo

* Respetar los requisitos documentados.
* No inventar funcionalidades.
* No modificar el alcance sin documentarlo.
* No considerar una interfaz HTML como funcionalidad implementada.
* Mantener separados frontend, backend y base de datos cuando corresponda.
* Respetar los actores definidos (Usuario, Validador, Administrador).
* Mantener los requisitos como referencia antes de implementar nuevas funcionalidades.

## 12. Relación con otros documentos

* **README.md** → contexto general y estado del proyecto.
* **docs/REQUISITOS.md** → requisitos y alcance (este documento).
* **docs/ARQUITECTURA.md** → arquitectura técnica.

> `docs/ARQUITECTURA.md` será creado posteriormente y todavía no debe considerarse implementado.