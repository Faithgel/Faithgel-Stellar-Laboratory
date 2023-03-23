---
{"dg-publish":true,"permalink":"/asignaturas/administracion-y-programacion-de-base-de-datos/administracion-y-programacion-de-base-de-datos/"}
---


# Administración de transacciones
```ad-check
title: ¿Que es una transaccion?
Una transacción en una base de datos es una serie de operaciones que se realizan como una unidad atómica e indivisible. Esto significa que si una parte de la transacción falla, todas las operaciones realizadas hasta ese momento se deshacen y se restaura el estado anterior a la transacción.
```

```ad-check
title: ACID
-   Atomicidad (Atomicity): significa que una transacción debe ser tratada como una unidad indivisible de trabajo. Si una parte de la transacción falla, toda la transacción debe ser revertida a su estado original.
    
-   Consistencia (Consistency): garantiza que una transacción llevará la base de datos de un estado válido a otro estado válido. En otras palabras, una transacción no puede violar las reglas de integridad de la base de datos.
    
-   Aislamiento (Isolation): asegura que cada transacción se ejecute de manera aislada de otras transacciones. Esto significa que cada transacción debe ser tratada como si fuera la única transacción que se está ejecutando en la base de datos.
    
-   Durabilidad (Durability): garantiza que una vez que una transacción se ha completado con éxito, sus cambios se mantendrán incluso en caso de fallo del sistema.
```
```ad-example
title: Ejemplo
collapse: true
Supongamos que tenemos una base de datos de un sistema de ventas en línea que contiene una tabla de pedidos y una tabla de inventario. Para agregar un nuevo pedido a la base de datos, se deben realizar varias operaciones, como actualizar el inventario, registrar el pedido y actualizar el estado del pago. Estas operaciones se pueden realizar como una transacción para garantizar la integridad de los datos.

Un ejemplo de una transacción en este escenario podría ser el siguiente:

1.  Iniciar la transacción.
2.  Verificar si los productos solicitados están en stock en la tabla de inventario.
3.  Si los productos están disponibles, actualizar la tabla de inventario para reflejar la disminución de la cantidad de productos disponibles.
4.  Registrar el pedido en la tabla de pedidos, incluyendo la información del cliente y los productos solicitados.
5.  Actualizar el estado del pago en la tabla de pedidos para indicar que se ha realizado el pago.
6.  Confirmar la transacción.

Si en algún momento de la transacción ocurre un error, como que uno de los productos solicitados no esté disponible en el inventario, se deshacen todas las operaciones realizadas hasta ese momento y se restaura el estado anterior a la transacción. De esta manera, se garantiza que la base de datos siempre esté en un estado consistente y que los datos sean precisos y confiables.
```
```ad-hint
title: Concurrencias y planificacion
La concurrencia se refiere a la capacidad de múltiples usuarios o procesos para acceder y modificar simultáneamente los datos almacenados en una base de datos. Cuando varios usuarios intentan acceder a los mismos datos al mismo tiempo, pueden surgir problemas de concurrencia, como bloqueos o inconsistencias en los datos. Para evitar estos problemas, los sistemas de gestión de bases de datos utilizan técnicas de control de concurrencia, como el bloqueo de registros y la transacción de control de concurrencia.

La planificación se refiere al proceso de determinar el orden en que se ejecutan las operaciones en una base de datos. La planificación es importante para garantizar la consistencia de los datos y la eficiencia de la base de datos. Los sistemas de gestión de bases de datos utilizan algoritmos de planificación para determinar el orden de ejecución de las operaciones en una transacción. Los algoritmos de planificación pueden ser basados en reglas o basados en costos, y pueden ser deterministas o probabilísticos.