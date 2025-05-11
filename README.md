# Aplicación de Microservicios

Este proyecto implementa una arquitectura de microservicios para una aplicación de gestión de proyectos y chat.

## Estructura del Proyecto

El proyecto está dividido en tres microservicios:

- **api**: Microservicio para gestión de proyectos y usuarios
- **chat**: Microservicio para el sistema de chat
- **web**: Aplicación web principal que se comunica con los microservicios

## Requisitos

- Python 3.8+
- pip

## Instalación

### 1. Microservicio API

```bash
cd api
pip install -r requirements.txt
```

### 2. Microservicio Chat

```bash
cd chat
pip install -r requirements.txt
```

### 3. Aplicación Web

```bash
cd web
pip install -r requirements.txt
```

## Ejecución

Inicia cada uno de los servicios en terminales diferentes:

### 1. Microservicio API (Puerto 5001)

```bash
python run_api.py
```

### 2. Microservicio Chat (Puerto 5002)

```bash
python run_chat.py
```

### 3. Aplicación Web (Puerto 5000)

```bash
python run.py
```

## Acceso

- Aplicación web: http://localhost:5000
- API REST: http://localhost:5001
- Servicio de chat: http://localhost:5002

## Autenticación

- La aplicación utiliza JWT para la autenticación entre la web y la API
- El servicio de chat utiliza una API key básica para la autenticación
- El usuario por defecto es: `admin` / `Admin123!`

## Endpoints API

### Usuarios
- GET /users - Obtener todos los usuarios
- GET /users/{id} - Obtener un usuario específico
- POST /users - Crear un usuario
- PUT /users/{id} - Actualizar un usuario
- DELETE /users/{id} - Eliminar un usuario

### Proyectos
- GET /projects - Obtener todos los proyectos
- GET /projects/{id} - Obtener un proyecto específico
- POST /projects - Crear un proyecto
- PUT /projects/{id} - Actualizar un proyecto
- DELETE /projects/{id} - Eliminar un proyecto

### Autenticación
- POST /auth/login - Iniciar sesión y obtener token JWT
