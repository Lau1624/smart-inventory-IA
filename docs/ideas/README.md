##Ideas para el proyecto {28-06-2026} (ultima actualizacion)
  -Veremos que es posible implementar y que no.
#Implementacion de IA
  -Buscar implementarla para que analice datos financieros, que ayuden al mantenimiento del comercio y entregue propuestas reales, en base a datos, para lograr aumentar ventas o reducir costos. (a priori, posibles             propuestas en el futuro)
    /Por ejemplo: Mencionar tanda de productos que estan por vencer.
    /Mencionar qué productos estan siendo sobre o infra vendidos, en un periodo de tiempo y proceda a recomendar acciones en base a la caracteristicas del producto (no solo dar "protocolos", Analizar el caso y en base a         patrones entregar una posible solucion).
    /Implementar la IA en diversas areas del sistema.
    
#Sistema de fidelidad para cliente
  -Buscar implementar un sistema de puntos para el cliente, buscando incentivar la compra de estos.
    /Mediante premios, sorteos, promociones, etc.
    /Pagina y/o app para que el cliente interactue.
      //Si se implementara la app, se podria enviar promociones generales y si se registra en la app, personalizadas en base a un historial de compras "relevantes".
    
#Sistema de avisos de stock
  -Avisos de falta de stock, con la finalidad de que nunca llegue a 0 (no es una restriccion).

#Sistema que permita el control, verificacion y actualizacion de stock
  -Sistema estandar de stock

#Integrar un sistema completo con IA
  -No solo en el stock, buscar implementar IA en otros aspectos, como una Herramienta para la toma de desiciones.

#inventario
  -fecha_caducidad_producto (podria hacerlo por tandas, creo que muchas unidades de un mismo producto pueden tener fecha de vencimientos similares, por lo tanto aqui podria calcular una media entre unas fechas de           caducidad proximas, tener un promedio, para por lo menos poder avisar de que estan o proximas a vencer o ya vencieron, no un listado de cada unidad de producto, demaciados datos volatiles, todo el tiempo saliendo        (eliminando) y entrando esos datos, podriamos hacer por tandas o grupos de un mismo producto que estas tandas, serian "conjuntos de unidades" con fechas similares o muy proximas. Asociando unidades de productos con       estas tandas, para poder avisar de su caducidad y sabemos que tanda estan por vencer, si aun existen unidades de esta tanda que no se vendieron. Se podria aconsejar prioridad a estos a punto de vencer)

##eventos
  #lista
  
    -Un cliente-(1)
    1.1.Compra productos.
    1.2.Devuelve productos.
    1.3.Hace un pedido, para buscar o delibery.
    -Un empleado-(2)
    2.1.Realiza un conteo de inventario.
    2.2.Repone productos en gondola.
    2.3.Cocina producto.
    2.4.Ingresa producto en almacen
    2.5.
    -Un gerente-(3)
    3.1.Asigna tareas.
    3.2.Realiza pedidos de cotizacion
    3.3.Realiza pedidos de productos
    3.4.Realiza pedidos de insumos
    3.5.

  #acontecimientos por eventos
    
    -cliente-(1)
    1.1. Un cliente envia una lista de productos (para su compra) esta lista se compone de, producto y cantidad, a la hora de escanear el codigo de barra de un producto, suma la cantidades de productos del mismo tipo, se verifica su precio y se cobra, el cliente dispone de multiple metodos de pago, QR, tarjeta, efectivo, en caso de efectivo el personal debera validar la transferencia. 
    1.2. Un cliente encuentra un vencimiento, falla o simplemente desea devolver el producto, si posee el ticket correspondiente y el producto esta en optimas condiciones, el producto caduco o la falla del producto tenia garantia, se devuelve el monto acordado, un porcentaje del total o la completitud de la compra. Y se descarta este producto si no esta en optimas condiciones.
    1.3. Un cliente entra a la pagina web o aplicacion para realizar una lista de productos para su reserva, para busqueda o delibery. Existe un limite del cual se pueden reservar sin hacer delibery directo. Si el cliente desea comprar "mayorista" este limite se amplia pero la reserva se debera de realizar con tiempo para el retiro o flete del pedido.
    -empleado-(2)
    2.1. Un empleado realiza el conteo de inventario, puede ser por sector o completo, la finalidad de eeste es controlar el inventario y realizar ajustes para mantener el sistema de logistica lo mas exacto posible. Se tomara un listado por sector y producto, de estos la cantidad contada al menos proxima, de esto se determinara si existe una diferencia significativa como para ajustar el inventario del sistema o control el stock o posibles robos.
    2.2. Un empleado repone productos en gondolas asignadas, estos productos se obtienen de los lotes y se hara una salida de inventario a las gondolas en formato fifo con prioridad a los productos con fechas de vencimiento mas cercanos que contengan plazos de vencimientos sostenibles, no aquellos productos que estan muy cercanos a vencer y tienen probabilidades mas altas de dejar una mancha en la reputacion de la empresa, Se daran recomendaciones en caso de que se encuentre existencias a punto de caducar.
    2.3. Un empleado cocina comida para el sector de alimentos frescos (pollos, ensaladas, carnes, empanadas, etc.).
    2.4. Un empleado ingresa cargas de productos o lotes al almacen para su almacenamiento y logistica.
    -Gerente-(3)
    3.1. Asignacion de tareas laborales como conteos, lavados de sectores, seguridad, etc.
    
