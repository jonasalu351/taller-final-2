# taller-final-2
Sistema Logístico – Puerto de Buenaventura  
Gestión de Lotes por Fecha (AVL) y Pedidos FIFO

Este proyecto implementa un sistema logístico para la gestión de mercancías en el Puerto de Buenaventura.  
El sistema utiliza:

Árbol AVL** para almacenar los lotes de productos ordenados por su **fecha de vencimiento (AAAAMMDD)**.  
Colas FIFO** asociadas a cada lote para manejar pedidos de despacho.  
 Menú interactivo por consola para registrar mercancía, pedidos, cancelaciones y reportes.

 Características principales

 Gestión de Lotes (AVL)
Cada lote contiene:
- Fecha de vencimiento  
- Nombre del producto  
- Stock disponible  
- Cola FIFO de pedidos

El árbol AVL garantiza que las operaciones de búsqueda, inserción y eliminación se realicen en **O(log n)**.

 Gestión de Pedidos (Cola FIFO)
Cada lote mantiene su cola FIFO con:
- Destino  
- Cantidad solicitada  

Los pedidos se procesan en el orden en que fueron registrados.

 Funcionalidades del Menú
 Recepción de Mercancía
- Inserta un nuevo lote en el AVL.  
- No permite fechas duplicadas.  
- El nombre del producto se convierte automáticamente a mayúsculas.

 Registrar Pedido de Despacho
- Selecciona automáticamente el lote más próximo a vencer.  
- Encola un pedido en su FIFO.  
- El stock se reduce según la cantidad solicitada.

  Cancelar Lote Completo
- Elimina el lote del AVL.  
- Libera toda la cola FIFO asociada.  
- Requiere confirmación del usuario.

 Cancelar un Pedido Específico
- Permite eliminar un pedido particular dentro de la cola FIFO de un lote.  
- Devuelve el stock asociado.

 Reporte de Estado (In-Order)
Muestra todos los lotes ordenados desde la fecha más cercana a vencer hasta la más lejana.  
Incluye:
- Fecha  
- Producto  
- Stock  
- Número de pedidos  
- Detalle de la cola FIFO

  Salir
- Libera toda la memoria del árbol y sus colas.  
- Cierra la aplicación.

 Tecnologías utilizadas

- **Lenguaje:** C  
- **Estructuras de datos:**  
  - Árbol AVL  
  - Cola FIFO (lista enlazada simple)  
- **Versión recomendada del compilador:** C11 o superior

-  SISTEMA LOGISTICO - PUERTO DE BUENAVENTURA
1. Recepcion de Mercancia (INSERTAR en AVL)
2. Registrar Pedido de Despacho (ENCOLAR en FIFO)
3. Cancelar Lote Completo (ELIMINACION EN AVL)
4. Cancelar un Pedido Especifico
5. Reporte de Estado (RECORRIDO IN-ORDER)
6. Salir
Seleccione una opcion:
