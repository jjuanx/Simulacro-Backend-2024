Se ha añadido tanto en la migration como en el model la siguiente propiedad a Restaurant :
    - promoted: Boolean 

Despues hemos creado una nueva ruta PATCH '/restaurants/:restaurantId/promote' , junto con un nuevo controlador 'promote':
    - Este nuevo controlador incluye una transaccion, donde primero se ha buscado el que tiene promoted = true, se le quita si existe, y despues etablecemos el que queremos como promoted=true

Posteriormente hemos añadido una nueva funcion a la validation para comprobar que no hay mas de un restaurante con promoted = true y por ultimo hemos establecido un order tanto en index, como en indexOner
