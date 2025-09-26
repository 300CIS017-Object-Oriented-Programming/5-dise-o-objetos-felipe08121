# Desarrollo del ejercicio 2

El diagrama describe un sistema de **gestión de pedidos** con tres clases: **Pedido**, **Plato** y **Cliente**.

Estas clases tienen los siguientes atributos y métodos:

    Pedido
    - + int numeroPedido  
    - + string estado  
    - + Cliente cliente  
    - + list platos  
    - No tiene métodos.  

    Plato
    - + string nombre  
    - + float precio  
    - No tiene métodos.  

    Cliente
    - + string nombre  
    - + string teléfono  
    - No tiene métodos.  

---

### Relaciones
- -> **Pedido pertenece (asociación) a Cliente.**  
- -> **Pedido contiene (agregación) a Plato.**

No tiene métodos y todos sus atributos son públicos.

---

### 1. R/
El sistema modelado describe un sistema de gestión de pedido, en el que cada Pedido contiene el número de pedido, el estado, un cliente (clase) asociado al pedido y una lista de platos (clases).  
A su vez, cada plato contiene un precio y un nombre, y cada cliente un nombre y un teléfono.  

Cada pedido puede tener muchos platos (lista, agregación), pero solo un cliente asociado a él (asociación).

---

### 2. R/
Sus relaciones son:

- -> **Pedido pertenece (asociación) a Cliente.**  
  **Importancia:** cada pedido está asociado a un solo cliente, lo que es importante para que no haya cruces entre los pedidos.  

- -> **Pedido contiene (agregación) a Plato.**  
  **Importancia:** cada pedido tiene una relación de agregación a Plato; es importante, ya que un solo cliente puede pedir muchos platos de diferente tipo.  

---

Por último, cabe destacar que todos los atributos son **públicos**, lo que significa que cualquiera puede ver y modificar los distintos atributos dentro de cualquier parte del código.