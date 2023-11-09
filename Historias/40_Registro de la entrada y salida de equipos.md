- Yo como: Administrador del inventario
- Quiero: Registrar la entrada y salida de equipos en el inventario
- Para: Mantener un seguimiento de los movimientos de los equipos

# Pendientes de definición
1.¿Se debe notificar al personal asignado cuando se registra la salida de un equipo?

#Especificación de requerimientos
1.El sistema debe permitir el registro de la entrada y salida de equipos en el inventario.
2.El sistema debe validar la información del equipo antes de registrar la entrada o salida.

#Análisis
El registro de la entrada y salida de equipos es crucial para mantener un seguimiento de los movimientos de los equipos en el inventario.
Se presiona el boton editable correspondiente y se permite al usuario modificar "Fecha de Entrega", "Fecha de Salida" y "estado"
![image](https://github.com/Crisale7/Invenio/assets/93544993/df608ccc-2a6f-4cb1-bb6e-db6d4eca4021)


#Criterios de aceptación
- Dado: Que el administrador ha ingresado la información de la entrada o salida de un equipo
- Cuando: El administrador intenta registrar la entrada o salida de un equipo en el inventario
- Entonces: El sistema debe validar la información y registrar la entrada o salida si es correcta

#Diseño
Request:

PUT BASE_URL/api/v1/inventario/{producto_id}
Content-Type: application/json
{
    "estado": "char",
    "fecha_entrada": "timestamp",
    "fecha_salida": "timestamp"
}

Response: Exitoso statusCode: 200

{
    "message": "Registro de entrada/salida actualizado con éxito"
}

Response: Error statusCode: 400

{
    "message": "Información de entrada/salida inválida"
}
