- Yo como: Usuario del sistema Invenio
- Quiero: Buscar equipos específicos en el inventario
- Para: Encontrar rápidamente los equipos que necesito

# Pendientes de definición
1. ¿Qué campos deben ser buscables?

# Especificación de requerimientos
1. El sistema debe permitir la búsqueda de equipos en el inventario.
2. El sistema debe proporcionar resultados de búsqueda relevantes basados en la consulta del usuario.

# Análisis
La capacidad de buscar equipos específicos en el inventario permite a los usuarios encontrar rápidamente los equipos que necesitan.
simplemente se selecciona el tipo de busqueda que deseamos tener y prosteriormente ingresar el dato relacionado al tipo de busqueda deseado y finalmente presionar el boton "Buscar"
![image](https://github.com/Crisale7/Invenio/assets/93544993/7cfbb867-bb97-4e0f-b8f4-c08e0ec93b3d)


# Criterios de aceptación
- Dado: Que el usuario ha ingresado una consulta de búsqueda
- Cuando: El usuario realiza una búsqueda en el inventario
- Entonces: El sistema debe mostrar los equipos que coinciden con la consulta de búsqueda

# Diseño
Request:


BASE_URL/api/v1/inventario/graficos?producto_id={producto_id}
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
    "message": "Error al realizar la búsqueda"
}
