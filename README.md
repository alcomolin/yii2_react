
# API REST Yii2

Se realizo un API REST con Yii2 para ser consumido desde un CRUD directamente en ReactJs, habilitando metodos para comunicar el Frontend con la base de datos en MySql, adicionalmente fue necesario habilitar CORS en el consumo de las API, ya que por utilizar puertos diferentes al realizar la peticion se toman como 2 sitios diferentes.

## API Reference

#### Obtener productos
Peticion GET para obtener todos los productos registrados para ser listados.
```http
  GET /web/api/product
```

#### Crear producto
Peticion POST para la creacion de un nuevo producto.
```http
  POST /web/api/product
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `name`      | `string` | Nombre del producto |
| `description`      | `string` | Descripcion del producto |
| `price`      | `integer` | precio del producto |
| `stock`      | `integer` | Cantidad del producto |

#### Editar producto
Peticion PUT para la edicion de productos ya registrados.
```http
  PUT /web/api/product/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `name`      | `string` | Nombre del producto |
| `description`      | `string` | Descripcion del producto |
| `price`      | `integer` | precio del producto |
| `Stock`      | `integer` | Cantidad del producto |

#### Eliminar producto
Peticion DELETE para la eliminacion de un producto registrado.
```http
  DELETE /web/api/product/${id}
```



## Appendix

* Se creo un modulo para la gestion de las peticiones del Frontend en la siguiente ruta:
    #### modules\api
#
* Se definio el filtro para los CORS y asi no presentar rechazos al realizar las peticiones por fuera del servicio de Yii en el archivo: 
    #### modules\api\controllers\ProductController.php
#
* Se crearon las reglas y los label de los atributos en el archivo:
    #### models\Product.php
#
* Se definio el ActiveQuery en el archivo: 
    #### models\ProductQuery.php
## Deployment

Para desplegar este proyecto, ejecute

* Ejecutar Wamp:
Iniciar una aplicacion que simule un servidor web con la carpeta del Backend.
* Probar la la Api Rest con este link:
  #### [Mostrar productos por GET](http://localhost/Blue_web_factory/yii2_react/web/api/product)

## Authors

- [@Alejandro Correa Molina](https://github.com/alcomolin)

