# EduTech IA - MVP

## Descripción
EduTech IA es una plataforma de educación personalizada que utiliza inteligencia artificial para recomendar cursos y contenidos adaptados a cada usuario. Este MVP (Producto Mínimo Viable) tiene como objetivo principal la creación de un sistema robusto y escalable basado en Java, aplicando principios de programación orientada a objetos.

## Tecnologías Utilizadas
- **Lenguaje de programación:** Java
- **Entorno de desarrollo:** IntelliJ IDEA
- **Control de versiones:** Git y GitHub
- **Compilación y gestión de dependencias:** Maven
- **Pruebas unitarias:** JUnit
- **Análisis de código:** SonarQube
- **Contenedores:** Docker
- **Integración y entrega continua:** GitHub Actions

## Arquitectura del Proyecto
El proyecto sigue una estructura basada en programación orientada a objetos con las siguientes clases principales:
- `Usuario` (abstracta): Base para `Alumno` y `Profesor`.
- `GestorDeCursos`: Administra los cursos disponibles.
- `Curso`: Permite a los alumnos inscribirse y gestionar contenido.
- `Filtro`: Selecciona cursos recomendados para los alumnos.
- `Contenido`: Maneja los materiales de aprendizaje.

## Flujo de Desarrollo
Se implementa un sistema de control de versiones basado en Git con las siguientes ramas:
- `main`: Rama estable con la última versión en producción.
- `develop`: Rama de integración donde se prueban nuevas características antes de pasar a `main`.
- Ramas de características (`feature/nombre-caracteristica`): Para el desarrollo de funcionalidades específicas.

### Proceso de Integración Continua (CI/CD)
1. Se realiza un `commit` en la rama de desarrollo.
2. Se ejecutan pruebas automáticas con JUnit y análisis de calidad con SonarQube.
3. Si las pruebas son exitosas, los cambios se fusionan en `develop`.
4. Una vez verificada la estabilidad, se genera un `pull request` a `main`.
5. Se despliega la nueva versión con Docker en un entorno de producción seguro.

## Seguridad y Buenas Prácticas
- Uso de permisos en GitHub para restringir cambios directos en `main`.
- Auditorías de seguridad periódicas con herramientas automatizadas.
- Implementación de copias de seguridad para prevenir pérdida de datos.
