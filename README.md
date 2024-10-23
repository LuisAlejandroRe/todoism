# Pipeline de CI con GitHub Actions para la Aplicación Todoism

Este repositorio demuestra la creación de un pipeline de Integración Continua (CI) utilizando **GitHub Actions**, el cual ejecuta pruebas automatizadas desde un repositorio externo usando **Playwright**. Las pruebas validan funcionalidades de la aplicación Todo, incluyendo:

1. **Creación de tareas**
2. **Marcar una tarea como completada**
3. **Limpiar las tareas**

Las pruebas se obtienen del repositorio [todoism-test](https://github.com/LuisAlejandroRe/todoism-test.git) y se ejecutan dentro de este pipeline de CI.

## Tabla de Contenidos

- [Descripción del Pipeline](#descripción-del-pipeline)
- [Pruebas](#pruebas)
- [Conclusión](#conclusión)

## Descripción del Pipeline

El pipeline se activa automáticamente en cada push o pull request a este repositorio. Recupera el conjunto de pruebas desde el repositorio [todoism-test](https://github.com/LuisAlejandroRe/todoism-test.git) y ejecuta las pruebas usando Playwright.El workflow está definido en el archivo .github/workflows/automated_test.yml. El pipeline de CI incluye los siguientes pasos:

1. **Checkout**: Descarga el código del repositorio actual.
2. **Clonar el Repositorio de Pruebas**: Clona el repositorio todoism-test que contiene las pruebas de Playwright.
3. **Configurar Node.js**: Configura el entorno de Node.js.
4. **Instalar Dependencias**: Instala las dependencias necesarias para ejecutar las pruebas.
5. **Ejecutar Pruebas**: Ejecuta el conjunto de pruebas de Playwright para validar las funcionalidades de la aplicación Todoism.

## Pruebas

Las pruebas están ubicadas en el repositorio externo [todoism-test](https://github.com/LuisAlejandroRe/todoism-test.git) y se centran en las siguientes características:

- **Crear Tarea**: Valida que una nueva tarea pueda ser creada y aparezca correctamente en la lista de tareas.
- **Completar Tarea**: Prueba la funcionalidad de marcar una tarea como completada.
- **Limpiar Tareas**: Asegura que las tareas sean eliminadas de la lista al hacer clic en el botón "Limpiar todo".

## Conclusión

Este repositorio implementa un pipeline de CI utilizando GitHub Actions, que ejecuta pruebas automatizadas con Playwright desde un repositorio externo. El pipeline valida funcionalidades de la aplicación Todoism, como la creación, el completado y la eliminación de tareas. El uso de pruebas automatizadas garantiza que la aplicación se mantenga estable y funcional ante nuevos cambios. Este ejercicio académico proporciona una aproximación práctica a la integración de pruebas automatizadas dentro de un flujo de integración continua, fortaleciendo la calidad y la robustez del ciclo completo de desarrollo de la aplicación.
