# sis257_cafeteria
## Descripcion de la Cafeteria
Este proyecto tiene como objetivo desarrollar un sistema para gestionar las operaciones de una cafetería. El sistema permitirá la administración de productos (bebidas, comidas), clientes, pedidos, empleados, control de inventario y ventas diarias, así como la gestión de proveedores y promociones.

## Entidades del negocio de Cafeteria

### 1. Productos
- **id_producto**: ID producto (PK).
- **nombre**: Nombre del producto 
- **categoría**: Tipo de producto 
- **precio**: Precio del producto.
- **tamaño**: Tamaño del producto 
- **descripción**: Descripción breve del producto.
- **estado**: Estado del producto (disponible/no disponible).

### 2. Clientes
- **id_cliente**: ID cliente (PK).
- **nombre**: Nombre completo del cliente.
- **correo**: Correo electrónico del cliente.
- **teléfono**: Número de teléfono del cliente.
- **dirección**: Dirección del cliente (opcional).
- **fecha_registro**: Fecha_registro del cliente en el sistema.

### 3. Pedidos
- **id_pedido**: ID pedido (PK).
- **id_cliente**: ID del cliente que realiza el pedido (FK).
- **fecha_pedido**: Fecha y hora del pedido.
- **estado**: Estado del pedido (en preparación, listo, entregado).
- **total**: Monto total del pedido.
 
### 4. Detalle de Pedido
- **id_detalle**: ID detalle_pedido (PK).
- **id_pedido**: ID del pedido asociado (FK).
- **id_producto**: ID del producto (FK).
- **cantidad**: Cantidad de productos solicitados.
- **precio_unitario**: Precio por unidad del producto en el momento del pedido.

### 5. Empleados
- **id_empleado**: ID empleado (PK).
- **nombre**: Nombre completo del empleado.
- **cargo**: Cargo del empleado 
- **teléfono**: Número de teléfono del empleado.
- **correo**: Correo electrónico del empleado.
- **fecha_contratación**: Fecha en la que fue contratado.
- **salario**: Salario mensual del empleado.

### 6. Inventario
- **id_producto**: ID del producto (FK).
- **stock**: Cantidad disponible del producto en inventario.
- **fecha_ingreso**: Fecha de ingreso del producto al inventario.
- **proveedor**: Nombre del proveedor que suministra el producto.

### 7. Proveedores
- **id_proveedor**: ID proveedor (PK).
- **nombre**: Nombre del proveedor.
- **teléfono**: Número de teléfono del proveedor.
- **correo**: Correo electrónico del proveedor.
- **dirección**: Dirección del proveedor.
- **productos_suministrados**: Lista de productos que el proveedor suministra.

### 8. Promociones
- **id_promoción**: ID promoción (PK).
- **nombre**: Nombre de la promoción 
- **descuento**: Porcentaje de descuento ofrecido.
- **fecha_inicio**: Fecha de inicio de la promoción.
- **fecha_fin**: Fecha de finalización de la promoción.
- **productos_incluidos**: Lista de productos incluidos en la promoción.

### 9. Reservas
- **id_reserva**: ID reserva (PK).
- **id_cliente**: ID del cliente que realiza la reserva (FK).
- **fecha_reserva**: Fecha de la reserva.
- **hora_reserva**: Hora de la reserva.
- **mesa**: Número de mesa reservada.
- **estado**: Estado de la reserva (confirmada, cancelada).

### 10. Pagos
- **id_pago**: ID pago (PK).
- **id_pedido**: ID del pedido asociado (FK).
- **método_pago**: Método de pago 
- **monto**: Monto total del pago.
- **fecha_pago**: Fecha y hora en que se realizó el pago.
- **estado**: Estado del pago (completado, pendiente).

## Instalación
1. Clonar el repositorio: `https://github.com/bea-18/sis257_cafeteria.git
2. Configurar la base de datos para el almacenamiento de productos, clientes, empleados, pedidos y otras entidades.

## Uso
El sistema permite gestionar:
- Productos del menú.
- Clientes registrados y no registrados.
- Pedidos de los clientes.
- Inventario de la cafetería.
- Gestión de empleados.
- Control de proveedores y productos suministrados.
- Implementación de promociones.
- Reservas de mesas.
- Pagos realizados por los clientes.
