# Documentación de Requerimientos - Sistema contable

## 1.Introducción

### 1.1 Propósito del Documento

Definir los requerimientos funcionales y no funcionales del sistema contable para la gestión de ventas, servicios, clientes y empleados de Avelinas Centro Integral de Belleza.

### 1.2 Alcance del Sistema

El sistema proporcionará una plataforma para administrar operaciones contables básicas, gestionar clientes, empleados, ventas de servicios y productos, con capacidad de expansión para reportes financieros y funcionalidades avanzadas.

### 1.3 Contexto del Negocio

Avelinas es un negocio local dedicado a ofrecer una amplia variedad de servicios de belleza, como manicura, pedicura, depilación, entre otros. Cuenta con un equipo de profesionales que trabajan bajo un modelo de ingresos por comisión: cada empleado recibe un porcentaje del valor de los servicios que realiza, con pagos quincenales o mensuales según corresponda.

Además de los servicios, el local comercializa productos relacionados con el cuidado personal, como cremas, esmaltes y otros artículos. Sin embargo, actualmente no cuentan con un sistema que integre de forma eficiente la gestión de ventas de productos con la liquidación de comisiones al personal. Tampoco disponen de herramientas que les permitan automatizar la generación de reportes o el cálculo de sueldos, lo que implica una carga administrativa manual propensa a errores y demoras.

Esta situación limita la visibilidad financiera del negocio, dificulta la toma de decisiones informadas y representa un desafío creciente a medida que el volumen de operaciones crece.

## 2.Descripción General

### 2.1 Perfil de Usuarios

- Administrador: acceso total al sistema.
- Contador: acceso a reportes financieros e información contable.

### 2.2 Ambiente Operativo

El sistema contable será una aplicación de escritorio para Sistemas Operativos Windows, instalada en los dispositivos autorizados. Su diseño contempla dos modalidades de acceso:

- **Puesto local:** una computadora ubicada en el negocio servirá como estación principal de trabajo.
- **Acceso remoto:** los dueños y/o administradores podrán instalar la misma aplicación en sus computadoras personales, desde donde podrán acceder al sistema de forma remota.

La información se almacenará centralizadamente en una base de datos en la nube, lo que garantiza integridad, disponibilidad y respaldo de los datos en tiempo real. El sistema contará con mecanismos de autenticación y control de acceso según el perfil del usuario.

## 3. Requerimientos Funcionales

### 3.1 Gestión de Clientes

- **RF-1.1:** El sistema permitirá registrar nuevos clientes con la siguiente información: nombre completo, correo, fecha de cumpleaños, teléfono.
- **RF-1.2:** El sistema permitirá consultar la información de los clientes.
- **RF-1.3:** El sistema permitirá modificar la información de los clientes.
- **RF-1.4:** El sistema permitirá inactivar clientes sin eliminarlos de la base de datos.
- **RF-1.5:** El sistema deberá permitir buscar clientes por id y nombre.

### 3.2 Gestión de Servicios

- **RF-2.1:** El sistema permitirá crear servicios con información de nombre, descripción, precio, lista de insumos(para calcular costo).
- **RF-2.2:** El sistema permitirá modificar la información de los servicios.
- **RF-2.3:** El sistema permitirá inactivar servicios sin eliminarlos.


### 3.3 Gestión de Empleados

- **RF-3.1:** El sistema permitirá registrar empleados con la siguiente información: nombre completo, teléfono, lista de comisiones por servicio.
- **RF-3.2:** El sistema permitirá modificar la información del empleado, como el teléfono y las comisiones por servicio.
- **RF-3.3:** El sistema permitirá registrar adelantos de sueldos a los empleados.
- **RF-3.4:** El sistema llevará un registro de los servicios realizados por el empleado.
- **RF-3.5:** El sistema permitirá registrar retiro/venta de productos para los empleados.
- **RF-3.6:** El sistema permitirá registrar retiro/venta de servicios para los empleados.

### 3.4 Ventas de Servicios

- **RF-4.1:** El sistema permitirá registrar una venta de servicio asociada a un cliente.
- **RF-4.2:** El sistema permitirá asignar un empleado a un servicio vendido.
- **RF-4.3:** El sistema calculará automáticamente el total de la venta incluyendo impuestos.
- **RF-4.4:** El sistema generará un número único de factura/comprobante para cada venta.
- **RF-4.5:** El sistema permitirá registrar el método de pago utilizado.
- **RF-4.6:** El sistema permitirá registrar ventas con pago pendiente.
- **RF-4.7:** El sistema permitirá registrar una venta de servicio asociada a un empleado.

### 3.5 Ventas de Productos

- **RF-5.1:** El sistema permitirá registrar una venta de producto asociada a un cliente.
- **RF-5.2:** El sistema calculará automáticamente el total de la venta incluyendo impuestos.
- **RF-5.3:** El sistema generará un número único de factura/comprobante para cada venta.
- **RF-5.4:** El sistema permitirá registrar el método de pago utilizado.
- **RF-5.5:** El sistema permitirá registrar ventas con pago pendiente.
- **RF-5.6:** El sistema modificará de forma automática el stock del o de los productos.
- **RF-5.7:** El sistema permitirá registrar una venta de producto asociada a un empleado.
- **RF'5.8:** El sistema permitirá registrar la devolución de un producto.

### 3.6 Registro Financiero

- **RF-6.1:** El sistema registrará todas las transacciones financieras.
- **RF-6.2:** El sistema permitirá registrar gastos operativos categorizados (e.j. gastos de inmueble).
- **RF-6.3:** El sistema permitirá generar un cierre de caja diario.
- **RF-6.4:** El sistema permitirá crear informes(comisiones ganadas de empleados, ganancias, etc.).
- **RF-6.5:** El sistema permitirá administrar cuentas contables.
- **RF-6.6:** El sistema permitirá crear Liquidación de Comisiones mensuales. (Teniendo en cuenta servicios dados, productos/servicios retirados, adelantos de sueldo).

### 3.7 Gestión de Insumos

- **RF-7.1:** El sistema permitirá registrar nuevos insumos con la siguiente información: nombre, costo por unidad.
- **RF-7.2:** El sistema permitirá actualizar los precios de los insumos.
- **RF-7.3:** El sistema permitirá eliminar insumos.

### 3.8 Gestión de Vauchers

- **RF-8.1:** El sistema permitirá la creación de vauchers con la siguiente información: nombre cliente, nombre destinatario, monto, fecha de vencimiento.
- **RF-8.2:** El sistema permitirá registrar el uso de un vaucher, actualizando el monto restante (Se puede utilizar en más de un servicio).
- **RF-8.3:** El sistema dará de baja automáticamente vauchers vencidos. 

## 4. Requerimientos no Funcionales

### 4.1 Seguridad

- **RNF-1.1:** El acceso al sistema requerira autenticación mediante usuario y contraseña.
- **RNF-1.2:** Las contraseñas se almacenarán encriptadas en la base de datos.
- **RNF-1.3:** El sistema implementará control de acceso basado en roles (RBAC).
- **RNF-1.4:** El sistema registrará un log de actividades críticas para auditoría.

### 4.2 Rendimiento

- **RNF-2.1:** El tiempo de respuesta para operaciones estandar no deberá superar los 2 segundos.
- **RNF-2.2:** La base de datos deberá optimizarse para consultas rápidas sobre datos frecuentes.

### 4.3 Disponibilidad

- **RNF-3.1:** El sistema deberá estar disponible durante las horas de operacion de la tienda y horas extras de trabajo.
- **RNF-3.2:** Se realizarán copias diarias de la información en horarios diurnos. 
- **RNF-3.3:** El sistema debe estar disponible para acceso remoto.

### 4.4 Usabilidad

- **RNF-4.1:** La interfaz debe ser intuitiva y requerir mínima capacitación.
- **RNF-4.2:** El flujo de venta debe completarse en menos de 5 pasos.

## 5. Reestricciones y Limitaciones

- El sistema debe operar sobre el Sistema Operativo Windows.