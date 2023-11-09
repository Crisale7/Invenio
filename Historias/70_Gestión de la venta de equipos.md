- Yo como: Administrador de ventas
- Quiero: Gestionar la venta de equipos desde el inventario
- Para: Mantener un registro de las ventas y asegurar que los equipos vendidos se retiren del inventario

# Pendientes de definición
1. ¿Cómo se debe manejar la facturación y el pago de las ventas?

# Especificación de requerimientos
1. El sistema debe permitir la gestión de las ventas de equipos.
2. El sistema debe actualizar el inventario para reflejar las ventas de equipos.

# Análisis
La gestión de las ventas de equipos es crucial para mantener un registro preciso de las ventas y para asegurar que los equipos vendidos se retiren del inventario.
![image](https://github.com/Crisale7/Invenio/assets/93544993/f89193b2-9cdf-4162-b801-348bba21315e)

# Criterios de aceptación
- Dado: Que el administrador ha marcado un equipo como vendido
- Cuando: El administrador registra la venta en el sistema
- Entonces: El sistema debe actualizar el inventario para reflejar la venta

# Diseño
Request:

PUT BASE_URL/api/v1/inventario/{producto_id}
Content-Type: application/json
Authorization: Bearer JWT
{
    "estado": "V"
}

Response: Exitoso statusCode: 200

{
    "message": "Estado del equipo actualizado con éxito"
}

Response: Error statusCode: 400

{
    "message": "Información de venta inválida"
}
