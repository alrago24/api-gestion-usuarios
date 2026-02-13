# Proyecto: API de Gestión de Usuarios


#### Estudiante: Alison Diaz

 URL de la API: [Gestion-usuarios] (https://698a98706c6f9ebe57ba22b3.mockapi.io/api/1/Usuarios)

## 1. Modelo de Datos Diseñado

Se configuro el recurso (USUARIOS) con la siguiente estructura de datos:
''' {
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
  '''

## 2. Bitácora de Operaciones CRUD(Respuesta de Postman)

### A. Obtener todos los registros (GET)

