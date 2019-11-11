# Arquitectura de Seguridad

# 1. Arquitectura

La Arquitectura IT está basada en la recolección y entendimiento de los requisitos de negocio.

Desarrollar una solución que encaje con estos requisitos.

Se requieren planes de arquitectura para las futuras necesidades de negocio.

La arquitectura es como construir una casa, con muchas piezas y todas tienen que encajar entre sí.

Tenemos:

- Componentes físicos
- Networks
- Operaciones
- Control de Acceso
- Continuidad de negocio
- Aplicaciones
- Criptografía

La arquitectura de seguridad se implementa en cada uno de los niveles de computación:

- Procesador individual
- Red local de ordenadores
- Red regional de ordenadores
- Enterprise network
- Cloud computing environments
- WWW

Los principios de arquiectura son:

- Interoperabilidad
- Integración
- Reutilización de componentes existentes
- Estandarización
- Facilitar el mantenimiento

# 2. Arquitecturas comunes

- P2P

    * Workstation conectada directamente contra otra semejante.

- Client-Server

    * Servidor principal que proporciona aplicaciones, o datos a otros workstations o dispositivos de la red.
    * Permite gestión y capacidad centralizada

- Arquitectura Centralizada

    * Un punto central que proporcionaa plicaciones, capacidad de computo y datos a unidades de negocio distribuidas.
    * Permite computación central y gestión.
    * Ventajas: Permite rapidos cambios de seguridad
    * Desventajas: Puede causar problemas a las unidades de negocio distribuidas

- Arquiectura Descentralizada

    * Los servidores del punto central se utilizan como agencia de coordinación y seguimiento.
    * Cada unidad de negocio distribuida es responsable de planificar y ejecutar los cambios cuando tengan el mínimo impacto operacional.
    * Ventajas: Menos probable de causar un impacto operacional.
    * Desventajas: Puede ser lento implementar parches de seguridad en caso de emergencia.
    * A menudo requirere una aproximación diplomática hacia la seguridad.

- Open Architecture

    * Las especificaciones son públicas para los diseñadores
    * Incluye estandard aprobados y arquitecturas diseñadas de forma privada.
    * Opuesto a arquitecturas cerradas o propietarias.
    * Linux es un buen ejemplo de esto.

Cada arquitectura tiene sus ventajas o inconvenientes.

Un arquitecto no es un ingeniero.

__Ingeniero__: Construye y configura sistemas
__Arquitecto__: Planea como los ingenieros pueden hacer eficiente su trabajo.

- Cloud Architecture

    * Ofrece algunas tecnologías que proporcionan la seguridad deseada.
    * Ofrece muchas ventajas y soluciones
    * Para nuevas organizaciones, cabe preguntarse antes el porqué no usarlo con todo lo que ofrece.
    * Puede ser interna, privada o externa

__Cloud Computing NIST SP800-145:__

La arquitectura cloud (o cloud computing) es un modelo para posibilitar la ubicuidad, acceso a sistemas compartidos tales como networks, servidores, almacenaje, aplicaciones y servicios que pueden ser rápidamente aprovisionados y desplegados con el mínimo esfuerzo de gestión incluso por el proveedor de servicios.

__Características Cloud__

- Servicio bajo demanda
- Amplio acceso a la red
- Pooling de recursos
- Muy elástico
- Se puede cuantificar el servicio facilmente

Hay diferentes tipos de Cloud:

- Public: incluso se ofrece púbico por razones de marketing, data mining, etc.
- Privado: usada por organizaciones gubernamentales, bancos, grandes corporaciones
- Híbrido: es una mezcla de los dos
- Community Cloud: Organizaciones con un objetivo común: Hospitales

__Cloud Service Models__

- Software as a service (Un servicio de base de datos online)
- Platform as a service (Amazon AWS, Openshift,.. )
- Infrastructure as a service (cualquier ordenador está en el cloud)

Beneficios:

- Capability Expenses vs Operational expenses.
- Acceso a personal muy cualificado del proveedor
- Disponibilidad

## 3. Aislamiento y memoria

- CPU
- System Memory Management
    * CPU Registers
    * Cache
    * Main Memory
    * Swap Files
- Memory Addressing
    * Logical
    * Relative
    * Physical
- Memory Management Requirements
    * Relocation
    * Protection
    * Sharing
- Memory Protection
    * Memory Reference
    * Different data classes
    * Users can share access
    * Users can't generate memory addresses
    * Aplicaciones no pueden acceder directamente a la memoria
    * Segmentation
    * Paginación
    * Protection keying
    * Secondary Storage

- Main Storage
    * Registers
    * Cache
    * RAM
- Secondary Storage
    * Internal
    * External
    * Virtual Memory
    * SANS
    * NAS
    * Clusters

La memoria se puede aislar de varias formas:

    * de forma Temporal
    * de forma Físical
    * de forma Virtual







