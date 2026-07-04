##Entidades
  #Persona (empleado, cliente)
    dni
    cuit
    nombre
    apellido
    fecha nacimiento
    
##inventario
  #Producto
    idproducto
    denominación
    estado

  #detalleproducto
    idproducto
    tipoventa
    categoria
    
  #categoria
    id
    categoriaproducto
    
  #tipoventa
    id
    unidad
    
        
  #unidad
    id 
    unidadtipo (grm, kg, metro, etc)
  
  #lotes
    idlote
    
##Finanzas 
  #facturas
    idfactura

  ##
