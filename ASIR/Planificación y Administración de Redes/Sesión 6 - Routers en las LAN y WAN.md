### LAN y WAN

**LAN (Local Area Network)**:

- **Definición**: Red de área local que conecta dispositivos dentro de un área geográfica limitada, como una oficina o un edificio.
- **Función/Propósito**: Facilitar la comunicación y el intercambio de recursos (archivos, impresoras, etc.) entre dispositivos cercanos.
- **Transmisión de datos**: Utiliza switches para dirigir datos a dispositivos específicos dentro de la red, basándose en direcciones MAC.
- **Switch**: Dispositivo que opera en la capa 2 (Enlace de Datos) y envía datos únicamente al puerto destino, mejorando la eficiencia.

**WAN (Wide Area Network)**:

- **Definición**: Red de área amplia que conecta múltiples LANs, cubriendo grandes distancias geográficas (por ejemplo, Internet).
- **Función/Propósito**: Conectar redes geográficamente dispersas, permitiendo comunicación entre diferentes ubicaciones.
- **Transmisión de datos**: Depende de routers para interconectar redes, utilizando direcciones IP y protocolos de enrutamiento.

### ¿Qué es un router?

- **Definición**: Dispositivo de red que opera en la **capa 3 (Red)** del modelo OSI, utilizando el **protocolo IP** para dirigir paquetes de datos entre redes diferentes.
- **Tablas de enrutamiento**: Almacenan información sobre rutas para enviar datos al destino correcto. Los protocolos de enrutamiento incluyen:
    - **RIP (Routing Information Protocol)**: Protocolo simple basado en distancia.
    - **OSPF (Open Shortest Path First)**: Protocolo avanzado que calcula rutas óptimas.
    - **EIGRP (Enhanced Interior Gateway Protocol)**: Protocolo propietario de Cisco, eficiente para redes grandes.
    - **BGP (Border Gateway Protocol)**: Utilizado en Internet para enrutamiento entre dominios.

### Comparación entre Hub, Switch y Router

El documento incluye una tabla comparativa que destaca las diferencias entre estos dispositivos:

|**Característica**|**Hub**|**Switch**|**Router**|
|---|---|---|---|
|**Capa OSI**|Capa 1 (Física)|Capa 2 (Enlace de Datos)|Capa 3 (Red)|
|**Inteligencia**|Ninguna, transmite a todos los puertos|Media, usa direcciones MAC|Alta, usa direcciones IP y tablas de enrutamiento|
|**Difusión del tráfico**|Envía a todos los puertos|Solo al puerto destino|Solo entre redes diferentes|
|**Dirección que maneja**|No maneja direcciones|Dirección MAC|Dirección IP|
|**Ideal para**|Redes pequeñas o antiguas|Redes modernas con alta demanda|Conectar LAN con WAN (Internet)|

### Tipos y funciones de los routers

- **Routers domésticos**: Utilizados en hogares para conectar dispositivos a Internet.
- **Routers empresariales**: Diseñados para redes corporativas, con mayor capacidad y funciones avanzadas.
- **Routers de borde (Edge routers)**: Conectan redes internas con redes externas, como Internet.
- **Routers Core**: Gestionan el tráfico dentro de grandes redes, como en proveedores de servicios.

**Razones para usar routers**:

- Conectar redes locales (LAN) con redes externas (WAN).
- Gestionar tráfico entre múltiples redes para garantizar acceso eficiente (Access Network).

### Funciones avanzadas de un router

- **NAT (Network Address Translation)**: Traduce direcciones IP públicas a privadas, permitiendo que múltiples dispositivos compartan una única IP pública.
- **DHCP (Dynamic Host Configuration Protocol)**: Asigna direcciones IP automáticamente a dispositivos en una red privada.
- **Firewall básico**: Filtra el tráfico de red para mejorar la seguridad.
- **ACL (Access Control List)**: Controla el acceso a dispositivos o recursos específicos en la red.
- **VPN (Virtual Private Network)**: Proporciona conexiones seguras y remotas, cifrando datos entre usuarios y servidores.

### Ejercicio práctico: Introducción a routers con Packet Tracer

El documento incluye preguntas relacionadas con el uso de routers en simulaciones con **Packet Tracer**, una herramienta para practicar configuraciones de red:

- **Diferencias físicas entre router y switch**: Los routers suelen tener puertos WAN y capacidades de enrutamiento avanzadas, mientras que los switches tienen más puertos Ethernet para conexiones locales.
- **Conexión directa de un PC al router**: Es posible, pero requiere configuración adecuada (por ejemplo, asignación de IP), ya que el router no actúa como un switch sin configuración.
- **Función de un router sin configurar**: Sin configuración, no puede enrutar tráfico ni asignar direcciones IP, quedando inactivo o limitado a funciones básicas.
- **Comunicación entre PCs conectados a un switch**: Los PCs no se comunican si no tienen direcciones IP asignadas o si el switch no está conectado a un router para redes externas.
- **Ubicación del router en una red grande**: Se coloca entre la LAN y la WAN, actuando como puerta de enlace (gateway).
- **Interfaces del router**: Ejemplo de un router con:
    - 1 puerto USB.
    - 1 puerto de consola.
    - 1 puerto GE RJ45 WAN.
    - 1 puerto GE RJ45 FortiLink.
    - 3 puertos GE RJ45 Ethernet.
    - Capacidad de 600 Mbps por puerto.