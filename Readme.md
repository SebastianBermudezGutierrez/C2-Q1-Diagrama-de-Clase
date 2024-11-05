# C2-Q1-Diagrama-de-Clase

´´´sql 
@startuml
 
Class Persona  {
  +TipoDocumento : String
  + NumeroDocumento : String
  + Nombres : String
  + Apellidos : String
  + Gmail : String
  + Telefono : String
  + Direccion: String
}

Class Usuario  {
+ Usuario : String
+ Contraseña : String
}

Class Rol  {
+ Codigo : String
+ Nombre : String
+ Descripcion : String
}

Class Modulo {
+ Codigo : String
+ Nombre : String
+ Descripcion : String
+ Ruta : String

}

Class Vista  {
+ Codigo : String
+ Nombre : String
+ Descripcion : String
+ Ruta : String
}
Class Modulo_Vista  {
+ Modulo : String
+ Vista : String
}



Class Categoria  {
+ Codigo : String
+ Nombre : String
+ Descripcion : String
}

Class Producto  {
+ Codigo : String
+ Nombre : String
+ Descripcion : String
+ Categoria : String
}

Class Inventario  {
+ Stock () : void
+ valorCompra () : void
+ valorRenta () : void
+ Sucursal () : void
+ Fecha () : Date
}
  
Class Empresa  {
+ NIT : String
+ Nombre : String
+ Direccion : String
+ Gmail : String
+ Telefono : String
+ Id : String
}

Class Sucursal  {
+ Nombre : String
+ Direccion : String
+ Gmail : String
+ Telefono : String

}
Class Factura  {
+ fechaVenta () : Date
+ valorBruto () : void
+ valor neto () : void
+ Descuento () : void
+ Pago : String
}

Class Detalle_Factura  {
+ Productos : String
+ Cantidad () : void
+ valorBruto () : void
+ valor neto () : void
+ Descuento () : void
}

Class Medio_Pago  {
+ Codigo : String
+ Nombre : String
+ Descripcion : String
}

Persona -- Usuario : Tiene
Usuario -- Rol : Su rol es
Modulo -- Rol : Depende del
Modulo -- Vista : Va con
Modulo_Vista -- Modulo : Relacion
Persona -- Modulo_Vista
Persona -- Empresa : Esta
Persona -- Producto : Elige
Producto -- Categoria : Pertenece a
Inventario -- Producto : Esta
Sucursal -- Empresa : Va con la
Persona -- Factura : Es
Factura -- Detalle_Factura : Sale
Usuario -- Medio_Pago 
Medio_Pago -- Factura : Con

## Diagrama Quiz

![Quiz1](https://github.com/user-attachments/assets/7e2a4eca-7755-41df-879c-f7c40b2bd759)
