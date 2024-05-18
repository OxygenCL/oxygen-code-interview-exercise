# Prueba Técnica para Desarrollador PHP en Laravel

## Introducción

Bienvenido/a a la prueba técnica. Queremos evaluar tus habilidades desarrollando una pequeña aplicación usando el framework Laravel. Sigue las instrucciones y entrega tu código al finalizar. Puedes usar cualquier recurso en línea si lo necesitas, pero asegúrate de que el código que entregues sea tuyo.

## Objetivo

Crear una aplicación web sencilla de gestión de tareas. La aplicación debe permitir a los usuarios:

1. Crear una cuenta e iniciar sesión.
2. Crear, editar y eliminar tareas.
3. Marcar las tareas como completadas o pendientes.
4. Ver una lista de todas sus tareas.

## Requisitos

### 1. Configuración del Proyecto

1. Haz fork de este repositorio.

2. Configura tu base de datos en el archivo `.env`. Puedes usar MySQL, SQLite, PostgreSQL, etc.

### 2. Autenticación

1. Puedes crear la autenticación desde cero pero te recomendamos usar una solución ya establecida de Laravel.

### 3. Modelo y Migración de Tareas

1. Crea un modelo y una migración para `Task`:
    ```bash
    php artisan make:model Task -m
    ```

2. En la migración, define, al menos, las siguientes columnas para la tabla `tasks`:
    - `title`
    - `description`
    - `is_completed`

3. Ejecuta las migraciones.

### 4. Relaciones y Controladores

1. Define la relación en el modelo `User` (un usuario tiene muchas tareas).

2. Define la relación en el modelo `Task` (una tarea pertenece a un usuario).

3. Crea un controlador de recursos para `Task`.

4. Implementa los métodos en `TaskController` para manejar las operaciones CRUD.

### 5. Rutas y Vistas

1. Define las rutas en `web.php`.

2. Crea las vistas necesarias en el directorio `resources/views/tasks`.

### 6. Validación y Seguridad

1. Asegúrate de validar los datos en los métodos `store` y `update` del controlador:
    ```php
        'title' => 'required|string|max:255',
        'description' => 'required|string',
    ```

2. Protege las rutas y controladores para asegurarte de que los usuarios solo puedan ver y modificar sus propias tareas.

## Entrega

1. Actualiza tu fork (puede ser privado) y comparte el enlace con nosotros.
2. Proporciona instrucciones claras sobre cómo configurar y ejecutar el proyecto.

### Notas Adicionales

- Considera usar Eloquent para interactuar con la base de datos.
- Es recomendable utilizar Blade para las vistas.
- Puedes agregar características adicionales si tienes tiempo, como la paginación en la lista de tareas o la búsqueda.

¡Buena suerte!
