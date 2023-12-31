- Yo como: Administrador del sistema Invenio
- Quiero: Registrar nuevos usuarios en el sistema
- Para: Permitir a los nuevos usuarios acceder y utilizar el sistema

# Pendientes de definición
1. ¿Se requiere validar la información del usuario antes de registrarla en el sistema?
2. ¿Qué roles y permisos se deben asignar a los nuevos usuarios?

# Especificación de requerimientos
1. El sistema debe permitir el registro de nuevos usuarios.
2. El sistema debe validar la información del usuario antes de registrarla.

#Análisis
El registro de usuarios en el sistema es esencial para controlar el acceso al sistema y garantizar que solo los usuarios autorizados puedan utilizarlo.
Donde solo sebe ingresar su Email y contraseña para posteriormente presionar el boton "enviar".
En caso de querer registrarse con Google simplemente presionar el boton "Registrese con Google"
![image](https://github.com/Crisale7/Invenio/assets/93544993/48c291d0-17a6-4d65-8810-b8131977194d)


#Criterios de aceptación
- Dado: Que el administrador ha ingresado la información del usuario
- Cuando: El administrador intenta registrar un nuevo usuario en el sistema
- Entonces: El sistema debe validar la información y registrar al usuario si es correcta

#Diseño
Request:

POST BASE_URL/api/v1/usuarios
Content-Type: application/json
{
    "usuario": "string",
    "contraseña": "string"
}

Response: Exitoso statusCode: 201

{
    "personal_id": int
}

Response: Error statusCode: 400

{
    "message": "Información del usuario inválida"
}
