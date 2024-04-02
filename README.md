# Configuración de Code Owners🚀

## Introducción

Este proyecto utiliza un enfoque estructurado para la configuración de Code Owners, facilitando la asignación de revisores a las áreas específicas del código fuente. A continuación, se describe el proceso de configuración y la herramienta utilizada para automatizar la inyección de Code Owners en los pipelines.

## Archivo CODEOWNERS y Template 📚

El archivo CODEOWNERS define las asignaciones de revisores para rutas específicas del código fuente. Para facilitar la configuración, se proporciona un template en [codeowners_template.txt](CODEOWNERS-injection/codeowners_template.txt). Asegúrate de seguir este template al configurar el archivo CODEOWNERS.

## Herramienta de Inyección (CODEOWNERS-injections)📦

Para automatizar la inyección del archivo CODEOWNERS con las configuraciones y el template mencionado anteriormente, utilizamos la herramienta [CODEOWNERS-injection](https://github.com/BancoBice/CODEOWNERS-injection). Esta herramienta agiliza el proceso de configuración, asegurando consistencia y eficiencia en las migraciones.

### Pasos para la Inyección 🤝

1. Clona el repositorio [CODEOWNERS-injection](https://github.com/BancoBice/CODEOWNERS-injection).
2. Utiliza la herramienta para inyectar el archivo CODEOWNERS en los pipelines de tu proyecto.
3. Confirma que la inyección se ha realizado correctamente y sigue las pautas del template.

## Implementación en Ramas Main y Develop

La configuración de Code Owners se implementará en las ramas Main y Develop del repositorio. Esto garantiza que las asignaciones de revisores estén vigentes en las ramas principales de desarrollo.

## Creación de la Estructura src/.github

En caso de que el directorio `src/.github` no exista, se creará automáticamente durante la implementación. Este directorio contendrá el archivo CODEOWNERS, asegurando que la estructura necesaria esté presente.

## Secretos

El flujo de trabajo utiliza un secreto GH_PAT, que debe ser un Token de Acceso Personal de GitHub del usuario agregado en el repositories.json con los permisos necesarios para crear repositorios, configurar protecciones de ramas y crear variables de repositorio.

---

## Estructura del json

Es necesario detallar el owner del repositorio y el usuario

```json
    {
        "owner": "BancoBice",
        "user": "userex_bice",
        "repositories": [
            {"repo_name": "SISVYSCTR-ms-login-legacy"},
            {"repo_name": "SISVYSCTR-osb-acl-telo-4010"},
            {"repo_name": "SISVYSCTR-osb-utilesClaveAcceso"}
        ]
    }
