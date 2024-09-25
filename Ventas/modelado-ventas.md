# Modelado de Base de Datos

## List Entities

### Clients **(ED)**
- cliente_id
- name
- lastname
- phone **(UQ)**
- email  **(UQ)**
- direccion
- cp
- ciudad
- pais_id **(FK)**

### Products **(ED|EC)**

- product_id **(PK)**
- name
- description
- img
- price
- stock

### sells **(ED)**

- sell_id **(PK)**
- client_id **(FK)**
- date
- total_price

### products_x_sells **(EP)**

- product_sells_id **(PK)**
- sell_id **(FK)**
- product_id **(FK)**
- stock_product

### country **(EC)**

- country_id **(PK)**
- name
- domain **(UQ)**

## Relaciones

1. **client** has **country** (_1 - 1_).
1. **client** generates **sell** (_1 - M_).
1. **sell** has **produc_sell** (_1 - M_).
1. **product_sell** is a **product** (_1 - 1_).

![Modelo Relacional](modelado-ventas-diagrama.svg)