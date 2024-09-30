# sis257_cafeteria
Descripcion
Este proyecto tiene como objetivo desarrollar un sistema para gestionar las operaciones de una cafetería. El sistema permitirá la administración de productos (bebidas, comidas), clientes, pedidos, empleados, control de inventario y ventas diarias, así como la gestión de proveedores y promociones.

Entidades del negocio
1. Productos
id_producto: ID único del producto (PK).
nombre: Nombre del producto (Ej: Café Americano, Capuccino).
categoría: Tipo de producto (Ej: Bebida, Comida).
precio: Precio del producto.
tamaño: Tamaño del producto (Ej: Pequeño, Mediano, Grande).
descripción: Descripción breve del producto.
estado: Estado del producto (disponible/no disponible).
2. Clientes
id_cliente: ID único del cliente (PK).
nombre: Nombre completo del cliente.
correo: Correo electrónico del cliente.
teléfono: Número de teléfono del cliente.
dirección: Dirección del cliente (opcional).
fecha_registro: Fecha en la que el cliente fue registrado en el sistema.
3. Pedidos
id_pedido: ID único del pedido (PK).
id_cliente: ID del cliente que realiza el pedido (FK).
fecha_pedido: Fecha y hora del pedido.
estado: Estado del pedido (en preparación, listo, entregado).
total: Monto total del pedido.
4. Detalle de Pedido
id_detalle: ID único del detalle del pedido (PK).
id_pedido: ID del pedido asociado (FK).
id_producto: ID del producto (FK).
cantidad: Cantidad de productos solicitados.
precio_unitario: Precio por unidad del producto en el momento del pedido.
5. Empleados
id_empleado: ID único del empleado (PK).
nombre: Nombre completo del empleado.
cargo: Cargo del empleado (Ej: Barista, Cajero).
teléfono: Número de teléfono del empleado.
correo: Correo electrónico del empleado.
fecha_contratación: Fecha en la que fue contratado.
salario: Salario mensual del empleado.
6. Inventario
id_producto: ID del producto (FK).
stock: Cantidad disponible del producto en inventario.
fecha_ingreso: Fecha de ingreso del producto al inventario.
proveedor: Nombre del proveedor que suministra el producto.
7. Proveedores
id_proveedor: ID único del proveedor (PK).
nombre: Nombre del proveedor.
teléfono: Número de teléfono del proveedor.
correo: Correo electrónico del proveedor.
dirección: Dirección del proveedor.
productos_suministrados: Lista de productos que el proveedor suministra.
8. Promociones
id_promoción: ID único de la promoción (PK).
nombre: Nombre de la promoción (Ej: 2x1 en café).
descuento: Porcentaje de descuento ofrecido.
fecha_inicio: Fecha de inicio de la promoción.
fecha_fin: Fecha de finalización de la promoción.
productos_incluidos: Lista de productos incluidos en la promoción.
9. Reservas
id_reserva: ID único de la reserva (PK).
id_cliente: ID del cliente que realiza la reserva (FK).
fecha_reserva: Fecha de la reserva.
hora_reserva: Hora de la reserva.
mesa: Número de mesa reservada.
estado: Estado de la reserva (confirmada, cancelada).
10. Pagos
id_pago: ID único del pago (PK).
id_pedido: ID del pedido asociado (FK).
método_pago: Método de pago (Ej: Tarjeta, Efectivo).
monto: Monto total del pago.
fecha_pago: Fecha y hora en que se realizó el pago.
estado: Estado del pago (completado, pendiente).
