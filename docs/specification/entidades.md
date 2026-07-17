##Entidades
  #persona (empleado, cliente)
    idpersona (si una persona es del extranjero no posee dni)
    dni
    nombre (string)
    apellido (string)
    fecha nacimiento (date)
    contacto(numerico)
    domicilio(string)

  #cliente
    idpersona fk
    puntos (float)
    idnivel fk
    
  #empleado
    idpersona fk
    
  #rolempleado
    idempleado fk (idpersona)
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
    
  #local
    idlocal
    contacto(numerico)
    direccion(string)
    idfranquicia
    
  #nivelbeneficio
    idnivel 
    nivel(string)
    descripcion(string)
    
  #beneficioxnivel
    idnivel fk
    idbeneficio fk
    
  #beneficio
    idbeneficio 
    descripcionbeneficio(string)
    idtipobeneficio fk
    valor (float)
    
  #tipobeneficio
    idtipobeneficio
    descripcion (string)
    
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

  #reposicion
    
  
  #movimientoinventario
    idmovimiento
    idlote fk
    idtipomovimiento fk
    cantidad
    fecha
    idventa fk null
    idlocal_destino FK NULL
    idempleado fk
    observacion null

  #tipomovimiento
    idtipomovimiento
    nombretipo (string)
    signofijo(int null )(+1/ -1)
    
  #conteoinventario
    idconteo 
    idlocal fk
    idsector fk null
    fechainicio
    fechacierre null
    estado (boole)

  #conteoempleado
    idconteo fk
    idempleado fk

  #detalleconteo
    idconteo fk
    idlote fk
    cantidadcontada
    cantidadsistema
    
  #almacenes
    idalmacen
    ubicacion(string)
    idlocal fk
    
  #zonaalmacenamiento
    idzona PK
    idalmacen FK
    capacidad (float)
    idunidad FK

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
    idsector 
    numero
    descripcion(string)
    idlocal fk
    
##Finanzas 
  #facturas
    idfactura

  ##
