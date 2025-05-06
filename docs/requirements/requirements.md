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
