- Yo como: Usuario del sistema Invenio
- Quiero: Ingresar al sistema de forma segura
- Para: Administrar el inventario de equipos

# Pendientes de definición
1. ¿Se requiere autenticación de dos factores para el ingreso al sistema?

# Especificación de requerimientos
1. El sistema debe permitir el ingreso de usuarios registrados.
2. El sistema debe validar las credenciales del usuario.

# Análisis
El ingreso al sistema es un paso crucial para garantizar que solo los usuarios autorizados puedan administrar el inventario.


# Criterios de aceptación
- Dado: Que el usuario ha ingresado sus credenciales
- Cuando: El usuario intenta ingresar al sistema
- Entonces: El sistema debe validar las credenciales y permitir el ingreso si son correctas

# Diseño
Request:

POST BASE_URL/api/v1/ingreso
Content-Type: application/json
{
    "usuario": "string",
    "contraseña": "string"
}

Response: Exitoso statusCode: 200

{
    "token": "string"
}

Response: No autorizado statusCode: 401

{
    "message": "Credenciales inválidas"
}