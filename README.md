# Proyecto-API-Veh-culos

**Estudiante:** Daniel Alejandro Muñoz Godoy

**URL de la API:** https://6987812b8bacd1d773ed9764.mockapi.io/Vehiculos

JSON
{
"marca": "string",
"modelo": "string",
"color": "string",
"precio": "number",
"disponible": "boolean",
"especificaciones": {
"motor": "string",
"transmision": "string",
"kilometraje": "number"
},
"mantenimiento": [
{
"fecha": "string",
"descripcion": "string"
}
]
} 2. Bitácora de Operaciones CRUD
A. Obtener todos los registros (GET)
Endpoint: /Vehiculos

Status: 200 OK

JSON
[
{
"id": "1",
"createdAt": "2024-02-21T05:38:36.012Z",
"marca": "Toyota",
"modelo": "Corolla",
"especificaciones": {
"motor": "1.8L",
"transmision": "Automática"
},
"mantenimiento": []
}
]
B. Creación de un nuevo registro (POST)
Endpoint: /Vehiculos

Status: 201 Created

Cuerpo de la petición:

JSON
{
"marca": "Tesla",
"modelo": "Model 3",
"color": "Blanco",
"precio": 42000.00,
"disponible": true,
"especificaciones": {
"motor": "Eléctrico",
"transmision": "Single Speed"
},
"mantenimiento": [
{ "fecha": "2024-01-10", "descripcion": "Revisión de software" }
]
}
Respuesta de Postman:

JSON
{
"id": "3",
"createdAt": "2024-02-21T16:45:00.000Z",
"marca": "Tesla",
"modelo": "Model 3",
"color": "Blanco",
"precio": 42000.00,
"disponible": true,
"especificaciones": {
"motor": "Eléctrico",
"transmision": "Single Speed"
},
"mantenimiento": [
{ "fecha": "2024-01-10", "descripcion": "Revisión de software" }
]
}
C. Consulta de registro individual (GET)
Endpoint: /Vehiculos/1

Status: 200 OK

JSON
{
"id": "1",
"marca": "Toyota",
"modelo": "Corolla",
"color": "Rojo",
"precio": 35000.00
}
D. Actualización de un registro (PUT)
Endpoint: /Vehiculos/1

Status: 200 OK

Modificación: Cambio de precio y color.

JSON
{
"marca": "Toyota",
"modelo": "Corolla",
"color": "Gris Plata",
"precio": 33000.00,
"disponible": true
}
E. Eliminación de un registro (DELETE)
Endpoint: /Vehiculos/1

Status: 200 OK

JSON
{
"id": "1",
"marca": "Toyota",
"modelo": "Corolla"
}
F. Validación de recurso inexistente (GET 404)
Endpoint: /Vehiculos/999

Status: 404 Not Found

Respuesta JSON:

JSON
{
"error": "Not found",
"message": "The resource with ID 999 does not exist in the database."
}
