
# Coding Challenge SYS

En este desafío, deberá procesar datos desde un archivo Json y realizar algunos cálculos para responder un par de preguntas que tiene nuestro equipo de métricas.


Puedes descargar el json como archivo en este repositorio

La estructura general del JSON  es:


```
proveedores[
    {     // Cada objeto representa uno de nuestros proveedores
        codigo,         // codigo interno del proveedor
        pais,          //  Pais de origen del proveedor
        nombre,         // Nombre del proveedor
        direccion { // Datos de la direccion
            estado,
            ciudad,
            calle,
            numero
        },         
        ordenes[
            { // Ordenes de compra hechas por el Proveedor
                numero_orden,
                fecha_creacion,
                fecha_llegada,
                transporte, // tipo de transporte aereo , terrestre , maritimo
                detalle [
                    {
                        producto,
                        cantidad,
                        precio

                    }
                ]
            }
        ]
    }
]
```


## Tu Tarea

Tienes que crear tres metodos:

    -   cantidadProveedoresPais() 
        Debes devolver un listado de la cantidad de proveedores que le compramos mercaderia por Pais.
        
    -   proveedorOrdenes()
        Debe devolver un listado de cada proveedor con su cantidad de ordenes de compra.
        
    -   montoTotalDolaresMes(int mes)
        Debe devolver la cantidad total comprada en el mes dado como parametro (son todas del año 2023)
