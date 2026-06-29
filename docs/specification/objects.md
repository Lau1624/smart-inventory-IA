Posibles objetos y funcionalidades que el sistema debe de tener: (todos deben responder a un requerimiento)
Clasificacion en base a su necesidad de los **"Objetos"** sin nada se da por entendido que son OBLIGATORIOS, DESEABLES son aquellas que no son necesarias para funcionar en las primeras versiones pero se busca implementar en el futuro y opcionales son aquellas que no son necesarias para la vida util del sistema.
{28-06-2026} (ultima actualizacion)
##Terminadores/Stakeholders
  #Personas
    -Clientes
      --Lista de posibles datos
          dni
          fecha_nacimiento
          cuit
          nombre y apellido
    -Empleados
      --Lista de posibles datos
          dni
          fecha_nacimiento
          cuit
          nombre y apellido
    -Distribuidores
      --Lista de posibles datos
          cuit
    -Proveedores
      --Lista de posibles datos
          cuit
    -Terceros
      --Lista de posibles datos
          cuit
    
  #No personas
    -Reloj
    -Calendario
    -IA

##Funcionalidades
  -Funcionalidades que existen para resolver requerimientos
  #inventario
    -fecha_caducidad_producto (podria hacerlo por tandas, creo que muchas unidades de un mismo producto pueden tener fecha de vencimientos similares, por lo tanto aqui podria calcular una media entre unas fechas de           caducidad proximas, tener un promedio, para por lo menos poder avisar de que estan o proximas a vencer o ya vencieron, no un listado de cada unidad de producto, demaciados datos volatiles, todo el tiempo saliendo        (eliminando) y entrando esos datos, podriamos hacer por tandas o grupos de un mismo producto que estas tandas, serian "conjuntos de unidades" con fechas similares o muy proximas. Asociando unidades de productos con       estas tandas, para poder avisar de su caducidad y sabemos que tanda estan por vencer, si aun existen unidades de esta tanda que no se vendieron. Se podria aconsejar prioridad a estos a punto de vencer)
      --Lista de posibles datos
        id_producto
        fecha_caducidad
    -Stock
      --Lista de posibles datos
        id_producto
        cantidad
    -Producto
      --Lista de posibles datos
        id_producto
        denominacion
        
    -muebles(opcional)
    -Utilidades (herramientas, moviles, etc)(deseable)
    
  #Compra y ventas
    -facturas
    -recibos
    -remitos
    -comprobantes

  #Control (especificar en el futuro)
  #Reportes (especificar en el futuro)
    /No se especifica pero podrian ser todo tipo de reportes, se veran cuales podrian ser y se clasficiara en base a su necesidad.
  #
