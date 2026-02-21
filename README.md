# Proyecto-API-Veh-culos

**Estudiante:** Daniel Alejandro Muñoz Godoy

**URL de la API:** [https://6987812b8bacd1d773ed9764.mockapi.io/Vehiculos](https://6987812b8bacd1d773ed9764.mockapi.io/Vehiculos)

```json
[
  {
    "createdAt": "2024-02-21T05:38:36.012Z",
    "marca": "Toyota",
    "modelo": "Corolla",
    "color": "Rojo",
    "precio": "35000.00",
    "disponible": true,
    "id": "1"
  },
  {
    "createdAt": "2024-02-21T10:15:20.150Z",
    "marca": "Ford",
    "modelo": "Mustang",
    "color": "Negro",
    "precio": "55000.00",
    "disponible": false,
    "id": "2"
  }
]
a => Obtener los registros (GET)
Status: 200 OK
[
  {
    "createdAt": "2024-02-21T05:38:36.012Z",
    "marca": "Toyota",
    "modelo": "Corolla",
    "color": "Rojo",
    "precio": "35000.00",
    "disponible": true,
    "id": "1"
  }
]

b=> Creación de un nuevo registro
Status: 201 Created

{
  "marca": "Tesla",
  "modelo": "Model 3",
  "color": "Blanco",
  "precio": "42000.00",
  "disponible": true
}

Respuesta  de POSMAN

{
  "createdAt": "2024-02-21T16:45:00.000Z",
  "marca": "Tesla",
  "modelo": "Model 3",
  "color": "Blanco",
  "precio": "42000.00",
  "disponible": true,
  "id": "3"
}

c=> Consulta de registro individual (GET)
Endpoint: /Vehiculos/1

Status: 200 OK

{
  "createdAt": "2024-02-21T05:38:36.012Z",
  "marca": "Toyota",
  "modelo": "Corolla",
  "color": "Rojo",
  "precio": "35000.00",
  "disponible": true,
  "id": "1"
}

d=> Actualización de un registro (PUT)
Status: 200 OK

Modificación: Cambio de precio y color del registro ID 1.
{
  "marca": "Toyota",
  "modelo": "Corolla",
  "color": "Gris Plata",
  "precio": "33000.00",
  "disponible": true,
  "id": "1"
}

e=> Eliminación de un registro
Status: 200 OK
{
  "marca": "Toyota",
  "modelo": "Corolla",
  "id": "1"
}

Operación	Método HTTP	Endpoint	Descripción	Código HTTP
Obtener todos	GET	/Vehiculos	Lista todos los vehículos del inventario	200 OK
Obtener por ID	GET	/Vehiculos/{id}	Devuelve un vehículo específico	200 OK
Crear registro	POST	/Vehiculos	Registra un nuevo vehículo en la API	201 Created
Actualizar registro	PUT	/Vehiculos/{id}	Modifica los datos de un vehículo existente	200 OK
Eliminar registro	DELETE	/Vehiculos/{id}	Elimina permanentemente un registro	200 OK
Recurso inexistente	GET	/Vehiculos/{id}	Error al consultar un ID que no existe	404 Not Found
```
