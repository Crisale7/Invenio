- Yo como: Usuario del sistema Invenio
- Quiero: Ver un listado de todos los equipos disponibles en el inventario
- Para: Tener una visión general de los equipos disponibles

# Pendientes de definición
1. ¿Se debe mostrar toda la información del equipo en el listado o solo algunos detalles clave?

# Especificación de requerimientos
1. El sistema debe proporcionar un listado de todos los equipos disponibles en el inventario.
2. El listado debe incluir detalles clave de cada equipo.

# Análisis
Proporcionar un listado de todos los equipos disponibles en el inventario permite a los usuarios tener una visión general rápida de los equipos.
![image](https://github.com/Crisale7/Invenio/assets/93544993/cbfc99b9-17bf-4c18-a951-788eec65c163)

# Criterios de aceptación
- Dado: Que el usuario ha ingresado al sistema
- Cuando: El usuario navega a la página de inventario
- Entonces: El sistema debe mostrar un listado de todos los equipos disponibles

# Diseño
Request:

GET BASE_URL/api/v1/inventory
Accept: Application/json

Response: Exitoso statusCode: 200

[
    {
        "producto_id": int,
        "modelo_id": int,
        "personal_id": int,
        "serie": "string",
        "estado": "char",
        "fecha_entrada": "timestamp",
        "fecha_salida": "timestamp"
    },
    ...
]

Response: Error statusCode: 400

{
    "message": "Error al obtener el listado de equipos"
}
