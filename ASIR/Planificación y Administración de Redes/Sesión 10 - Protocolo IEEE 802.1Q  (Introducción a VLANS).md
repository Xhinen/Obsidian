### ¿Qué es una VLAN?

**Definición**: Una VLAN (Red de Área Local Virtual) es una red lógica creada sobre una infraestructura física común, que agrupa dispositivos sin importar su ubicación física.

**Propósito**:

- **Segmentación**: Divide una red física en múltiples redes lógicas.
- **Rendimiento**: Mejora la eficiencia al reducir el tráfico innecesario.
- **Administración**: Optimiza el uso de recursos y facilita la gestión del tráfico.

**Ejemplos de aplicación**:

- **VLAN para contabilidad**: Restringe el acceso a recursos específicos del departamento de contabilidad.
- **VLAN para ventas**: Limita el acceso a recursos exclusivos del equipo de ventas.
- **VLAN para invitados**: Aísla completamente a los invitados de la red interna de la empresa.

### Conceptos fundamentales de VLANs - Segmentación

**Definición**: Las VLANs dividen una red física en varias redes lógicas, permitiendo la segmentación del tráfico.

**Mejoras clave**:

- **Seguridad**: Aísla el tráfico entre departamentos o áreas sensibles, reduciendo riesgos de acceso no autorizado.
- **Rendimiento**: Limita el tráfico de difusión (broadcast) dentro de cada VLAN, disminuyendo la congestión.
- **Gestión eficiente**: Simplifica la administración de dispositivos y tráfico, permitiendo políticas específicas por VLAN.

### Operación en Capa 2 y Capa 3

**Capa 2 (Enlace de Datos)**:

- Las VLANs operan en la capa 2 mediante switches.
- Utilizan el estándar **IEEE 802.1Q** para etiquetar tramas y segmentar el tráfico.
- Los dispositivos dentro de la misma VLAN se comunican directamente sin necesidad de enrutamiento.

**Capa 3 (Red)**:

- Para la comunicación entre VLANs, se requiere **enrutamiento entre VLANs**.
- Cada VLAN se asocia a una subred IP.
- Un **router** o un **switch de capa 3** gestiona el enrutamiento entre VLANs.

### Tipos de VLANs

1. **VLAN de Datos**:
    - Gestiona el tráfico general de usuarios (acceso a archivos, Internet, etc.).
2. **VLAN de Voz (VoIP)**:
    - Prioriza el tráfico de voz para garantizar la calidad de servicio (QoS).
    - Separa el tráfico VoIP del tráfico de datos.
3. **VLAN de Administración**:
    - Permite gestionar de forma segura dispositivos de red (switches, routers, firewalls).
4. **VLAN Nativa**:
    - VLAN predeterminada en enlaces troncales.
    - Las tramas sin etiquetas se asignan automáticamente a esta VLAN.

### ¿Qué es IEEE 802.1Q?

**Definición**: Estándar que permite transportar múltiples VLANs en una sola red física mediante el **etiquetado de tramas Ethernet**.

**Estructura de la etiqueta VLAN (4 bytes)**:

- **TPID (Tag Protocol Identifier, 16 bits)**: Identifica la trama como IEEE 802.1Q.
- **TCI (Tag Control Information, 16 bits)**:
    - **PCP (Priority Code Point, 3 bits)**: Define la prioridad del tráfico (QoS).
    - **DEI (Drop Eligible Indicator, 1 bit)**: Indica si la trama puede descartarse en caso de congestión.
    - **VID (VLAN Identifier, 12 bits)**: Identificador de la VLAN (rango: 1–4094).

**Funcionamiento**:

- Modifica la trama Ethernet insertando la etiqueta entre la dirección MAC de origen y el campo Ethertype.
- Soporta:
    - **Tramas etiquetadas (tagged)**: Para tráfico en enlaces troncales.
    - **Tramas no etiquetadas (untagged)**: Asignadas a la VLAN nativa.

### Beneficios de las VLANs

- **Aislamiento de tráfico**: Mejora la seguridad al evitar comunicación directa entre VLANs.
- **Optimización del ancho de banda**: El tráfico se limita a su VLAN, reduciendo congestión.
- **Mejor rendimiento y control**: Permite aplicar políticas específicas por VLAN (QoS, filtrado).
- **Reducción de costos**: Menor necesidad de hardware físico adicional.
- **Facilidad de gestión**: Redes lógicas más flexibles y manejables ante cambios.

### Tipos de tráfico en VLANs

1. **Tráfico etiquetado (Tagged)**:
    - Incluye la etiqueta IEEE 802.1Q.
    - Usado en **enlaces troncales** para transportar múltiples VLANs.
2. **Tráfico no etiquetado (Untagged)**:
    - Sin etiqueta.
    - Usado en **puertos de acceso**.
    - Asignado a la VLAN predeterminada (nativa).

### Implementación de VLANs en la práctica

**Configuración en switches**:

- Crear VLANs con identificadores únicos (1–4094).
- Asignar puertos como **access** (para dispositivos finales) o **trunk** (para enlaces entre switches).
- Usar etiquetado IEEE 802.1Q en enlaces troncales.

**Segmentación empresarial**:

- **Por seguridad**: Aplicar políticas de acceso específicas.
- **Eficiencia**: Reducir el tráfico de broadcast.
- **Administración**: Controlar el tráfico por departamentos o funciones.

**Ejemplo de configuración**:

- Crear una VLAN:
    
    text
    
    Copy
    
    `Switch(config)# vlan 10 Switch(config-vlan)# name Ventas`
    
- Configurar un puerto de acceso:
    
    text
    
    Copy
    
    `Switch(config)# interface fa0/1 Switch(config-if)# switchport mode access Switch(config-if)# switchport access vlan 10`
    
- Configurar un puerto troncal:
    
    text
    
    Copy
    
    `Switch(config)# interface fa0/24 Switch(config-if)# switchport mode trunk Switch(config-if)# switchport trunk allowed vlan 10,20,30`