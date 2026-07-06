##Entidades
  #persona (empleado, cliente)
    dni
    nombre (string)
    apellido (string)
    fecha nacimiento (date)
    roldepersona fk
    puntos (float)
    niveldebeneficios
    contacto(numerico)
    domicilio(string)
    
  #proveedores
    cuit
    contacto(numerico)
    ubicacion(string)
    
  #distribuidores
    iddistruibuidor
    contacto(numerico)
    direccion(string)
    
  #pedidoproducto (Existe para rastrear el proveedor del lote) (posibilidad de unir el modulo financiero con el modulo de inventario)
    idpedido
    idproveedor fk
    iddistribuidor fk
    fechapedido
    fechaingreso
    
  #detallepedido
    idpedido fk
    idproducto fk
    precio
    cantidadrecibida (aquel que se utilzara en lotes)
    cantidadsolicitada (dato por posible reclamo)
    
  #locales
    idlocal
    contacto(numerico)
    direccion(string)
  
  #nivelesbeneficios
    idbeneficio fk 
    tipobeneficio(string)
    descripcion(string)
    
  #roles
    idrol
    rol (string)
  
##inventario
  #producto
    idproducto (codigo de barra) (unico)
    denominación (string)
    estado (bool)
    tipoventa fk
    categoria fk
    
  #precioproducto
    idprecio 
    idproducto fk
    fechadesde
    fechahasta
    precio
    
  #categoria
    id
    categoriaxproducto(string)
    
  #tipoventa
    idtipoventa
    unidad fk
    nombre
    permitedecimales(bool)
    requierepeso(bool)
    
  #unidad
    idunidad
    unidadtipo( kg, metro, unidad))
  
  #lotes
    idlote
    iddetallepedido fk
    stock (float) (por ahora asi, ya que necesito medir kg, metro, unidad)
    fechaingreso
    idalmacen
    fechavencimiento
    
  #almacenes
    idalmacen
    ubicacion(string)
      
  #capacidadxalmacen (cada almacen tiene espacios reservados, donde puede abarcar x cantidad de x unidad)
    idcapacidad
    idalmacen

  #capacidadmaxima
    idcapacidad
    capacidad 
    unidad fk
    
  #inventario
    idinventario
    idlocal fk

  #lotexgondola
    id
    idgondola fk
    idlote fk
    cantidad 
  
  #gondola (asignacion de productos en gondolas, con un orden en sectores para que pueda existir un "mapa" para los clientes, conservando el orden)
    idgondola
    sector fk
    capacidadproductos
    tipogondola fk
    
  #tipogondola
    idtipogondola
    descripcion
    
  #sector
    idSector 
    numero
    descripcion(string)
    
    
##Finanzas 
  #facturas
    idfactura

  ##
