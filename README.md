# 🚗 Sistema de Gestión de Base de Datos — Concesionario de Vehículos

Este proyecto contiene el diseño lógico y relacional de una base de datos creada para administrar las operaciones principales de un concesionario de autos.

---

## 📌 ¿Qué hace esta Base de Datos?

El sistema está diseñado para organizar y gestionar 5 áreas clave del negocio:

1. **Vehículos (Inventario):** Control de autos en stock (marca, modelo, año, VIN único, precio, transmisión, combustible) y su disponibilidad.
2. **Clientes:** Registro de datos personales y de contacto para compras y mantenimientos.
3. **Vendedores:** Seguimiento del personal de ventas y sus transacciones asociadas.
4. **Ventas:** Registro de transacciones con fecha, método de pago, total y los vehículos incluidos en la compra.
5. **Mantenimientos:** Control de servicios técnicos (preventivos/correctivos) asignados a un vehículo y a un cliente (si aplica).

---

## 🛠️ Estructura del Modelo (6 Tablas)

* **`Salespeople`**: Datos del personal de ventas.
* **`Customers`**: Información de los clientes.
* **`Vehicles`**: Ficha técnica y estado del vehículo.
* **`Sales`**: Encabezado de la transacción de venta.
* **`Sale_Details`**: Tabla intermedia para vincular múltiples vehículos a una misma venta.
* **`Maintenance_Services`**: Historial de servicios técnicos.

---

## 🚀 Características Clave

* **Garantía de Unicidad:** El campo `VIN` (número de serie del auto) es único por vehículo.
* **Control de Inventario:** Cambios de estado en la disponibilidad del vehículo tras ser vendido.
* **Soporte de Mantenimiento Interno:** Permite registrar mantenimientos a vehículos en inventario aún no vendidos (cliente opcional).
