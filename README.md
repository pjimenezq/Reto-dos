# Reto dos
**Instrucción:** Elija un problema de la vida real (sistema de gestión de biblioteca, negocio de compra-venta, automóvil, etc) que se pueda modelar a través de objetos y clases. Plantee las relaciones de clases, composiciones, propiedades y comportamientos del sistema en uno mas diagramas tipo UML.

**Problema de la vida real**: Para este reto se tuvo como referencia una cafetería de comida rápida y las relaciones y comportamientos que existen entre el comprador, el vendedor y los distintos productos.

**Relación entre productos**

```mermaid

classDiagram
    class Productos
    Productos:+ Nombre
    Productos: + Precio

    Productos<|--Pizza

    class Pizza
    Pizza: + Tamaño
    Pizza: + Tipo de masa
    Pizza: + Ingredientes

    class Carnes
    class Pepperoni
    class Hawaiana

    Pizza<|--Carnes
    Carnes: + Sabor
    Carnes: + Aroma
    Pizza<|--Pepperoni
    Pepperoni: + Sabor
    Pepperoni: + Aroma
    Pizza<|--Hawaiana
    Hawaiana: + Sabor
    Hawaiana: + Aroma
    Productos<|--Helado

    class Helado
    Helado: + Tamaño
    Helado: + Toppings

    class Mora
    class Avellana
    class Arequipe
    Helado<|--Mora
    Helado<|--Avellana
    Helado<|--Arequipe
    Mora: + Sabor
    Mora: + Vegano
    Productos<|--Bebida
    Avellana: + Sabor
    Avellana: + Presencia de nueces
    Arequipe: + Sabor
    Arequipe: + Azúcar añadido
    class Bebida
    Bebida: + Temperatura

    class Agua
    Agua: + Sabor
    Agua: + Tamaño
    class Cerveza
    Cerveza: + Sabor
    Cerveza: + Alcohol
    class Jugo
    Jugo: + Sabor
    Jugo: + Adición de azúcar

    Bebida<|--Agua
    Bebida<|--Cerveza
    Bebida<|--Jugo

```

**Relación cliente-vendedor**

```mermaid
classDiagram
    class Cliente
    Cliente: + Humano
    Cliente: + Pedir productos()
    Cliente: + Consumir productos()
    Cliente: + Pagar productos()

    class Vendedor
    Vendedor: + Humano
    Vendedor: + Informar disponibilidad productos()
    Vendedor: + Tomar pedido()
    Vendedor: + Entregar productos()
    Vendedor: + Facturar los productos()

    Cliente--Vendedor

```
    
