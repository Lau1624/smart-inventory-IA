##Desiciones sobre el dominio del problema y requerimientos.
  -(Aun se está determinando el dominio, los requerimientos y el alcance del nuevo sistema)
  #Varios: (aun no los clasifico)
    -Un código de barras identifica el producto, no la unidad.
    -La trazabilidad por lote se pierde cuando los productos pasan a una góndola sin identificación individual.
    -El sistema debe admitir distintos niveles de trazabilidad según el tipo de producto.
    -Se busca evitar redundancias de datos.
    -Se debe admitir cambios en el tiempo
    
  #Inventario:
    -Podria tener "Lotes", en base a, por ahora, caducidad, donde tendria prioridad a la hora de reponer stock, aquellos con una caducidad mas proxima, en base a un criterio de seleccion, "si un lote esta por                    vencer demasiado pronto, se recomendará acciones, ya que simplemente darle prioridad, podria afectar a los clientes y por consecuente al rubro (empresa, organizacion, etc.))
    -Se debe de poseer datos necesarios para lograr una trazabilidad clara y eficiente.
    -Se debe de poder distinguir de forma sencilla entre productos.
    -Se debe poder almacenar los datos
    
  #Stock
    -Se debe de poder contabilizar la cantidad de unidades de un mismo producto.
    -Se debe lograr una trazabilidad de la cantidad de productos en movimiento (compra (suma de stock), venta (resta de stock), o perdidas (vencimientos, robos, etc.)).
    -Se debe poder almacenar los datos
    
  #Financiero (Aun determinando el dominio)
    -Se debe de poder rastrear las salidas y entradas de cualquier producto, insumo o objeto que se utilice dentro de la organizacion.
    -Se debe de poder facturar.
    -Se debe poder almacenar los datos de facturacion.

  #Personas
    -Se debe almacenar los datos de las personas (empleados, clientes y otros (podrian existir personas que interactuen en el sistema pero no sean empleados directos ni clientes (deja abierto la posibilidad a expansion))).
    -Se debe de poder trazabilizar cualquier interaccion de personas que incida en datos relevantes, un ejemplo: "cualquier movimiento de productos, dinero, etc".
