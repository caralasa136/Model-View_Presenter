# Modelo vista presentador (MVP)

>MVP es un patrón arquitectónico de interfaz de usuario diseñada para facilitar pruebas de unidad automatizada y mejorar la separación de inquietudes en lógica de presentación:

+ El modelo es una interfaz que define los datos que se mostrará o no actuado en la interfaz de usuario.
+ El presentador actúa sobre el modelo y la vista. Recupera datos de los repositorios (el modelo), y los formatea para mostrarlos en la vista.
+ La vista es una interfaz pasiva que exhibe datos (el modelo) y órdenes de usuario de las rutas (eventos) al presentador para actuar sobre los datos.

El grado de la lógica permitida en la vista varía entre las diferentes implementaciones. En un extremo, la vista es totalmente pasiva, reenviar todas las operaciones de interacción para el presentador. En esta formulación, cuando un usuario activa un método de evento de la vista, que no hace más que invocar un método del presentador que no tiene parámetros y no devuelve ningún valor. El presentador recupera entonces datos de la vista a través de los métodos definidos por la interfaz de vista. Por último, el presentador opera en el modelo y actualiza la vista con los resultados de la operación. Otras versiones de modelo-vista-presentador permiten cierta libertad con respecto a qué clase maneja una determinada interacción, evento o comandos. Esto suele ser más adecuado para arquitecturas basadas en la Web, donde la vista, que se ejecuta en el navegador de un cliente, puede ser el mejor lugar para manejar una interacción o comando en particular.

Desde un punto de vista de capas, la clase de presentador podría considerarse como perteneciente a la capa de aplicación en un sistema de arquitectura multicapa, pero también pueda ser visto como capa de presentador de su propiedad entre la capa de aplicación y la capa de interfaz del usuario.

![Modelo vista presentador](https://upload.wikimedia.org/wikipedia/commons/3/31/Modelo_Vista_Presentador_IGU_Patron_Dise%C3%B1o.png)

Aquí hya algunas de las principales diferencias entre Modelo Vista Presentador (MVP) y Modelo Vista Controlador (MVC):

![alt text](http://www.codeproject.com/KB/architecture/MVC_MVP_Differences/difftable.png)