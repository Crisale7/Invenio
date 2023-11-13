- Yo como: Administrador del inventario
- Quiero: Generar gráficos que muestren la actividad del inventario
- Para: Tener una visión clara de la actividad del inventario y poder tomar decisiones informadas

# Pendientes de definición 
1. ¿Qué métricas deben incluirse en los gráficos?

# Especificación de requerimientos 
1. El sistema debe permitir la generación de gráficos basados en la actividad del inventario.
2. Los gráficos deben incluir métricas relevantes para la gestión del inventario.

# Análisis 
La generación de gráficos basados en la actividad del inventario proporciona una visión visual clara de la actividad del inventario, lo que facilita la toma de decisiones informadas. Para esta pantalla, solo es necesario presionar el apartado “Gráficos” y los mismos se verán desplegados.

![image](https://github.com/Crisale7/Invenio/assets/93544993/59da45c7-d1e7-4e9b-9e93-d661e7ebba06)


# Criterios de aceptación 
- Dado: Que el administrador ha seleccionado un artículo del inventario
- Cuando: El administrador solicita la generación de un gráfico
- Entonces: El sistema debe generar un gráfico que muestre la actividad del artículo del inventario

Diseño Request:

GET BASE_URL/api/v1/inventario/graficos?producto_id={producto_id} Accept: Application/json

Response: Exitoso statusCode: 200

{ “datos_grafico”: {…} }

Response: Error statusCode: 400

{ “message”: “Error al generar los gráficos” }
