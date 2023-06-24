PRÁCTICA 2

DIAGRAMA DE CASOS DE USO DEL SISTEMA

                  +------------------------+
                  |    Sistema de Ventas   |
                  +------------------------+
                            |
                            |
        +-----------------------------------+
        |                                   |
   +----+----+                         +----+-----+
   | Gerente |                         |  Cajero  |
   +----+----+                         +----+-----+
        |                                   |
   +----+-------------------+     +---------+---------+
   | Registro de Venta    |     | Reporte de Ventas  |
   +----------------------+     +--------------------+
   | Control de Usuarios  |     | Control de Aperitivos |
   +----------------------+     +----------------------+


   DIAGRAMAS DE CLASES

         +-------------------------+
         |       SistemaVentas     |
         +-------------------------+
         |                         |
         |                         |
+-------------------+    +---------------------+
|   RegistroVenta   |    |   ReporteVentas     |
+-------------------+    +---------------------+
| -ventaId: int     |    | -ventas: Venta[]    |
| -fecha: Date      |    |                     |
| -total: double    |    +---------------------+
| -usuario: Usuario |
+-------------------+
         |
         |
         |
+-------------------+
|      Usuario      |
+-------------------+
| -userId: int      |
| -nombre: String   |
| -rol: Rol         |
+-------------------+
         |
         |
         |
+-------------------+
|       Rol         |
+-------------------+
| -rolId: int       |
| -nombre: String   |
+-------------------+


DIAGRAMAS DE DESPLIEGUE

        +------------------------+
        |   Nodo del Servidor    |
        +------------------------+
                  |
   +--------------+--------------+
   |                             |
+--+-------+             +-------+---+
|  Base   |             |  Cliente |
| de Datos |             |         |
+----------+             +---------+

