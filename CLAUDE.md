
# CLAUDE.md — PrintFlow

## 1. Contexto del proyecto

PrintFlow es una plataforma SaaS multiempresa orientada a negocios de publicidad, DTF, sublimación, bordados, estampados, vinilos y producción gráfica.

El sistema permitirá gestionar clientes, pedidos, cotizaciones, ingresos, gastos, finanzas, inventario y suscripciones.

El objetivo es desarrollar un producto comercializable mediante planes de suscripción mensual.

## 2. Stack tecnológico

Frontend:
- HTML5
- CSS3
- JavaScript Vanilla.

Backend:
- Java 21.
- Spring Boot.
- Spring Data JPA.
- Spring Security.
- Maven.

Base de datos:
- PostgreSQL.
- Flyway para migraciones.

Herramientas:
- Git y GitHub.
- Docker.
- Postman.

## 3. Arquitectura

Utilizar un monolito modular organizado por dominios funcionales.

Cada módulo debe mantener responsabilidades claras.

Los controladores gestionan las solicitudes HTTP.
Los servicios contienen las reglas de negocio.
Los repositorios gestionan el acceso a datos.
Las entidades representan el modelo persistente.

El frontend se comunica exclusivamente con el backend mediante API REST.

## 4. Reglas de desarrollo

- Mantener el código organizado y legible.
- Aplicar principios SOLID cuando corresponda.
- Evitar duplicación de código.
- Utilizar nombres descriptivos.
- Mantener responsabilidades separadas.
- Validar los datos recibidos.
- Manejar correctamente las excepciones.
- No agregar dependencias innecesarias.
- No introducir frameworks frontend sin autorización.
- No utilizar SQL directamente desde JavaScript.

## 5. Multi-tenancy

PrintFlow debe garantizar el aislamiento de información entre empresas.

Las operaciones relacionadas con información empresarial deben validar el contexto de la empresa autenticada.

Nunca confiar en un tenant_id proporcionado libremente por el frontend.

No permitir que una empresa consulte, modifique o elimine información perteneciente a otra.

## 6. Seguridad

- Nunca almacenar contraseñas en texto plano.
- No exponer secretos ni credenciales.
- Utilizar variables de entorno para configuraciones sensibles.
- Validar permisos en el backend.
- Proteger los endpoints.
- No almacenar datos de tarjetas bancarias.

## 7. Base de datos

- Utilizar PostgreSQL.
- Diseñar relaciones coherentes.
- Utilizar claves primarias y foráneas.
- Mantener integridad referencial.
- Gestionar cambios del esquema mediante Flyway.
- Evitar modificaciones manuales del esquema que no estén documentadas.

## 8. Metodología de trabajo

Trabajar mediante tareas pequeñas y verificables.

Antes de implementar:
1. Explicar qué se va a realizar.
2. Identificar los archivos involucrados.
3. Explicar las decisiones técnicas.

Después de implementar:
1. Explicar qué se modificó.
2. Explicar cómo funciona.
3. Ejecutar o proponer pruebas.
4. Informar errores y limitaciones.

## 9. Git

Utilizar Conventional Commits.

Prefijos:
- feat
- fix
- docs
- style
- refactor
- test
- chore

No realizar commits ni push sin autorización explícita del propietario del proyecto.

No modificar archivos ajenos a la tarea solicitada.

## 10. Restricciones

- No desarrollar funcionalidades que no hayan sido solicitadas.
- No modificar la arquitectura sin justificarlo.
- No generar código innecesariamente complejo.
- No asumir que una funcionalidad está terminada sin probarla.
- No inventar resultados de pruebas.
- No eliminar código existente sin explicar el motivo.

## 11. Forma de trabajo

El propietario del proyecto está aprendiendo desarrollo de software.

Por lo tanto, explicar las implementaciones de forma didáctica, detallando qué hace cada componente, por qué se utiliza y cómo se relaciona con el resto del sistema.

Claude actúa como asistente de programación, no como responsable autónomo de las decisiones arquitectónicas.
