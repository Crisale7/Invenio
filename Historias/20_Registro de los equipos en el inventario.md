- Yo como: Administrador del inventario
- Quiero: Registrar equipos en el inventario
- Para: Mantener un registro actualizado de todos los equipos disponibles

# Pendientes de definición
1. ¿Se requiere validar la información del equipo antes de registrarla en el inventario?

# Especificación de requerimientos
1. El sistema debe permitir el registro de nuevos equipos en el inventario.
2. El sistema debe validar la información del equipo antes de registrarla.

# Análisis
El registro de equipos en el inventario es esencial para mantener un control adecuado de los equipos disponibles.
Donde se debe llenar todos los apartados solicitados para el registro de un equipo y posteriormente presionar el boton "Guardar" o "Cancelar" Correspondiente
![image](https://github.com/Crisale7/Invenio/assets/93544993/aeb90e76-2c4a-4cae-a1ac-ff9c362c9b15) 


# Criterios de aceptación
- Dado: Que el administrador ha ingresado la información del equipo
- Cuando: El administrador intenta registrar un nuevo equipo en el inventario
- Entonces: El sistema debe validar la información y registrar el equipo si es correcta

# Diseño
Request:

POST BASE_URL/api/v1/inventario
Content-Type: application/json
{
    "serie": varchar,
    "tipo_producto": varchar,
    "modelo": "varchar",
    "estado": "char",
    "fecha_entrada": "timestamp",
    "fecha_salida": "timestamp",
    "usuario_id": "timestamp",
    "ram": "varchar",
    "memoria": "varchar",
    "procesador": "varchar",
}

Response: Exitoso statusCode: 201

{
    "producto_id": int
}

Response: Error statusCode: 400

{
    "message": "Información del equipo inválida"
}

