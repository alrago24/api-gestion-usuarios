# Proyecto: API de Gestión de Usuarios


#### Estudiante: Alison Diaz

 URL de la API: [Gestion-usuarios] (https://698a98706c6f9ebe57ba22b3.mockapi.io/api/1/Usuarios)

## 1. Modelo de Datos Diseñado

Se configuró el recurso `USUARIOS` con la siguiente estructura de datos:
```json
{
    "Nombre": "Juan",
    "Apellido": "Perez",
    "Cargo": "Asesor",
    "Servicio": {
      "Area": "Cambios voluntarios",
      "Atencion": "Front",
      "Idioma": "Ingles",
      "Nivel": "Experto"
    },
    "Turno": [
      "Manana",
      "tarde",
      "Noche"
    ],
    "Activo": true,
    "id": "1"
  }
  ```

## 2. Bitácora de Operaciones CRUD(Respuesta de Postman)

### A. Obtener todos los registros (GET)
- Status code: `200`
- Respuesta de Postman:

```json
[
    {
        "Nombre": "Juan",
        "Apellido": "Perez",
        "Cargo": "Asesor",
        "Servicio": {
            "Area": "Cambios voluntarios",
            "Atencion": "Front",
            "Idioma": "Ingles",
            "Nivel": "Experto"
        },
        "Turno": [
            "Manana",
            "tarde",
            "Noche"
        ],
        "Activo": true,
        "id": "1"
    },
    {
        "Nombre": "Maria",
        "Apellido": "Lopez",
        "Cargo": "Asesor",
        "Servicio": {
            "Area": "Eventos Operacionales",
            "Atencion": "Front",
            "Idioma": "Portugues",
            "Nivel": "Inicial"
        },
        "Turno": [
            "Manana",
            "tarde",
            "Noche"
        ],
        "Activo": false,
        "id": "2"
    },
    {
        "Nombre": "Daniel",
        "Apellido": "Ceballos",
        "Cargo": "Analista",
        "Servicio": {
            "Area": "Ventas",
            "Atencion": "Front",
            "Idioma": "Espanol",
            "Nivel": "Experto"
        },
        "Turno": [
            "Manana",
            "tarde",
            "Noche",
            "Mixto"
        ],
        "Activo": true,
        "id": "3"
    },
    {
        "Nombre": "Paula",
        "Apellido": "Herrera",
        "Cargo": "Asesor",
        "Servicio": {
            "Area": "Informacion y asesoria",
            "Atencion": "BackOffice",
            "Idioma": "Espanol",
            "Nivel": "Medio"
        },
        "Turno": [
            "Manana",
            "tarde",
            "Noche"
        ],
        "Activo": true,
        "id": "4"
    },
    {
        "Nombre": "Carlos",
        "Apellido": "Sanchez",
        "Cargo": "Asesor",
        "Servicio": {
            "Area": "Mentor",
            "Atencion": "BackOffice",
            "Idioma": "Frances",
            "Nivel": "Experto"
        },
        "Turno": [
            "Manana",
            "tarde",
            "Noche",
            "Mixto"
        ],
        "Activo": false,
        "id": "5"
    }
]
```

### B. Creación de un nuevo registro (POST)
- Status code:  `201 Created`
- Cuerpo enviado en Postman:

```json
{
    "Nombre": "Ricardo",
    "Apellido": "Gonzalez",
    "Cargo": "Supervisor",
    "Servicio": {
      "Area": "Pagos y Servicios",
      "Atencion": "BackOffice",
      "Idioma": "Español",
      "Nivel": "Experto"
    },
    "Turno": [
      "Manana",
      "tarde",
      "Noche",
      "Mixto"
    ],
    "Activo": true
  }
```
- Respuesta de Postman:

```json
{
    "Nombre": "Ricardo",
    "Apellido": "Gonzalez",
    "Cargo": "Supervisor",
    "Servicio": {
        "Area": "Pagos y Servicios",
        "Atencion": "BackOffice",
        "Idioma": "Español",
        "Nivel": "Experto"
    },
    "Turno": [
        "Manana",
        "tarde",
        "Noche",
        "Mixto"
    ],
    "Activo": true,
    "id": "6"
}
```

### C. Consulta de registro individual (GET) 
- Endpoint: /Usuarios/4
- Status Code: `200 OK`
- Respuesta de Postman:

```json
{
    "Nombre": "Paula",
    "Apellido": "Herrera",
    "Cargo": "Asesor",
    "Servicio": {
        "Area": "Informacion y asesoria",
        "Atencion": "BackOffice",
        "Idioma": "Espanol",
        "Nivel": "Medio"
    },
    "Turno": [
        "Manana",
        "tarde",
        "Noche"
    ],
    "Activo": true,
    "id": "4"
}
```

### D. Actualización de un registro (PUT)
- Status Code: `200 OK`
- Modificación: Se actualizó el turno, idioma y el estado del registro con ID 5
- Respuesta de Postman:

```json
{
    "Nombre": "Ricardo",
    "Apellido": "Gonzalez",
    "Cargo": "Supervisor",
    "Servicio": {
        "Area": "Pagos y Servicios",
        "Atencion": "BackOffice",
        "Idioma": "Ingles",
        "Nivel": "Experto"
    },
    "Turno": [
        "tarde",
        "Noche",
        "Mixto"
    ],
    "Activo": false,
    "id": "5"
}
```

### E. Eliminación de un registro (DELETE)
- Status Code: `200 OK`
- Respuesta de Postman:

```json
{
    "Nombre": "Maria",
    "Apellido": "Lopez",
    "Cargo": "Asesor",
    "Servicio": {
        "Area": "Eventos Operacionales",
        "Atencion": "Front",
        "Idioma": "Portugues",
        "Nivel": "Inicial"
    },
    "Turno": [
        "Manana",
        "tarde",
        "Noche"
    ],
    "Activo": false,
    "id": "2"
}
```

### F. Validación de Recurso inexistente (GET 404)
- Status Code: `404 Not Found`
- Respuesta de Postman:

```json
"Not found"
```

## 3. Resumen de Endpoints y Códigos HTTP

| Acción | Método | Endpoint | Código HTTP |
| :--- | :--- | :--- | :--- |
| Listar todo | GET | `/Usuarios` | 200 OK |
| Crear | POST | `/Usuarios` | 201 Created |
| Ver por ID | GET | `/Usuarios/4` | 200 OK |
| Actualizar | PUT | `/Usuarios/5` | 200 OK |
| Borrar | DELETE | `/Usuarios/2` | 200 OK |
| Error | GET | `/Usuarios/2` | 404 Not Found |