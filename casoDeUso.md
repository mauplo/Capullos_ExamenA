![Diagrama de Casos de Uso](casoDeUso.png)


# Caso de Uso
Mediante lucid modelalamos el sistema de pedidos para la aplicación Cafe ITAM, incorporando recomendaciones basadas en IA y una integración con el sistema institucional para hacer login y cargos en la colegiatura.  
- El objetivo del sistema es permitir a estudiantes realizar pedidos de manera eficiente y facilitar el control de inventario para cajeros y managers.

## Actores

| Actor | Tipo | Descripción |
|------|------|-------------|
| **Estudiante** | Primario | Usuario principal del sistema. Puede iniciar sesión, revisar el menú con recomendaciones personalizadas, realizar/cancelar pedidos y seleccionar método de pago. |
| **Cajero** | Secundario | Reacciona a todos los tickets. Puede consultar pedidos y ver detalles necesarios para entregarlos.  Inicia sesión para procesar y completar pedidos. |
| **Manager** | Secundario | Supervisa inventario, agrega productos, consulta predicciones de demanda basadas en IA y actualiza existencia de artículos. |


## Sistemas involucrados
| Sistema | Función |
|--------|---------|
| **Cafetería ITAM (Sistema principal)** | Interfaz para realizar  y gestionar pedidos, menú y pagos. |
| **API de Cafetería** | Base de datos de la cafeteria para modificar y consultar tablas relevantes al menú, tickets, inventario. |
| **Sistema del ITAM** | Sistema administrativo donde se verifican accesos y se permite el cargo a colegiatura del estudiante. |

---

## Casos de Uso Principales

### 🟡 **Compartidos** 
- **Login**
  - *Include:* `Verificar` *(Sistema ITAM)*
  - *Extend:* `Error Message` 
- **Verificar y Actualizar Existencias** *(API Cafeteria)*
- **Modificar Tickets** *(API Cafeteria)*
  
### 🔵 **Estudiante** 
- **Ver Menú con Recomendaciones IA**
- **Hacer Pedido**
  - *Include:* `Escoger Artículo`
  - *Include:* `Método de Pago`
  - *Include:* `Verificar y actualizar existencias` *(API Cafeteria)*
  - *Include:* `Modificar tabla de ticket` *(API Cafeteria)*
    - **Opciones de pago:**
      - `Pago Presencial`
      - `Cargo a Colegiatura` *(Sistema ITAM)*
  - *Extend:* `Error Message` (si no se puede procesar ej. no hay existencias)
- **Schedule (Programar Recogida)**
- **Cancelar Pedido**
  - *Extend:* `Error Message`
  - *Include:* `Consultar tabla ticket` *(API Cafeteria)*
  - *Include:* `Verificar y actualizar existencias` *(API Cafeteria)*

### 🟢 **Cajero** 
- **Revisar Pedidos**
  - *Include:* `Consultar tabla ticket` *(API Cafeteria)*
- **Completar Pedidos**
  - *Include:* `Modificar tabla de ticket` *(API Cafeteria)*

### 🟣 **Manager**
- **Agregar Producto**
  - *Include:* `Modificar tabla de menu` *(API Cafeteria)*
  - *Include:* `Detalle de Productos` 
- **Predicciones IA para Inventario**

---

## 🔗 LINK a lucid

https://lucid.app/lucidchart/850ed2f0-adaa-4773-a6ac-d35dd61b781a/edit?view_items=fdO6JK8BB3a-&page=0_0&invitationId=inv_49ba3e1e-379b-4603-9afd-c902488b980c


