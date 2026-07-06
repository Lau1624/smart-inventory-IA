##Entidades
  #persona (empleado, cliente)
    idpersona
    dni
    nombre (string)
    apellido (string)
    fecha nacimiento (date)
    contacto(numerico)
    domicilio(string)

  #cliente
    dni fk
    puntos (float)
    niveldebeneficios fk
    
  #empleado
    dni fk
    
  #rolempleado
    dni fk
    idrol fk
    fechainicio
    fechafinal
    
  #rolelaboral
    idrol
    roldescripcion (string)
    
  #proveedores
    idorganizacion fk 
    
  #distribuidores
    idorganizacion fk 
    
  #pedidoproducto (Existe para rastrear el proveedor del lote) (posibilidad de unir el modulo financiero con el modulo de inventario)
    idpedido
    idproveedor fk
    iddistribuidor fk
    fechapedido
    fechaingreso
    idlocal fk
    
  #detallepedido
    iddetalle
    idpedido fk
    idproducto fk
    precio
    cantidadrecibida (aquel que se utilzara en lotes)
    cantidadsolicitada (dato por posible reclamo)
    
  #franquicia
    idfranquicia 
    razonsocial
    cuit (unique)
    contacto
    fechainiciocontrato
    fechafincontrato NULL
    
  #locales
    idlocal
    contacto(numerico)
    direccion(string)
    idfranquicia
    
  #nivelesbeneficios
    idnivel 
    nivel(string)
    descripcion(string)
    
  #beneficioxnivel
    idnivel fk
    idbeneficio fk
    
  #beneficios
    idbeneficio 
    descripcionbeneficio(string)
    
  #organizacion 
    idorganizacion pk
    cuit (unique)
    razonsocial (string)
    contacto (numerico)
    ubicacion (string)
  
##inventario
  #producto
    idproducto 
    codigodebarra
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
    idlocal fk
    
  #categoria
    idcategoria
    nombre(string)
    idcategoriapadre fk null
    
  #tipoventa
    idtipoventa
    unidad fk
    nombre
    
  #unidad
    idunidad
    unidadtipo( kg, metro, unidad))
  
  #lotes
    idlote
    iddetallepedido fk null
    idordenproduccion fk null
    idproducto fk
    stock (float) (por ahora asi, ya que necesito medir kg, metro, unidad)
    idalmacen fk
    fechavencimiento

  #ordenproduccion
    idordenproduccion pk
    idlocal
    idproducto fk
    idempleado fk
    fecha
    cantidadproducida
  
  #movimientoventas
    idmovimiento
    idlote fk
    idtipomovimiento fk
    cantidad
    fechaingreso
    idventa fk null
    idpedido FK NULL
    idlocal_destino FK NULL
    idempleado fk
    observacion null

  #tipomovimiento
    idtipomovimiento
    nombretipo (string)
    signo(+1/ -1)
    
  #conteoinventario
    idconteo 
    idlocal fk
    idsector fk null
    fechainicio
    fechacierre null
    estado (boole)

  #conteoempleado
    idconteo fk
    idlempleado fk

  #detalleconteo
    idconteo fk
    idlote fk
    cantidadcontada
  
  #almacenes
    idalmacen
    ubicacion(string)
    idlocales fk
    
  #zonaalmacenamiento (cada almacen tiene espacios reservados, donde puede abarcar x cantidad de x unidad)
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
    capacidad (float)
    tipogondola fk
    unidad fk
      
  #tipogondola
    idtipogondola
    descripcion
    
  #sector
    idSector 
    numero
    descripcion(string)
    idlocal fk
    
##Finanzas 
  #facturas
    idfactura

  ##
