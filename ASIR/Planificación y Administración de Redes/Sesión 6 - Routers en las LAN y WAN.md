### LAN (Local Area Network) y WAN (Wide Area Network)

**LAN**:

- **Definición**: Red de área local que conecta dispositivos en un área geográfica limitada, como una oficina o edificio.
- **Función/Propósito**: Facilitar la comunicación y el intercambio de recursos (archivos, impresoras) entre dispositivos cercanos.
- **Transmisión de datos**: Utiliza switches para dirigir datos a dispositivos específicos basándose en direcciones MAC.
- **Switch**: Dispositivo de capa 2 (Enlace de Datos) que envía datos solo al puerto destino, optimizando el tráfico.

**WAN**:

- **Definición**: Red de área amplia que conecta múltiples LANs a través de grandes distancias, como Internet.
- **Función/Propósito**: Permitir la comunicación entre redes geográficamente dispersas.
- **Transmisión de datos**: Depende de routers para interconectar redes, utilizando direcciones IP y protocolos de enrutamiento.

### ¿Qué es un router?

**Definición**: Dispositivo de red que opera en la **capa 3 (Red)** del modelo OSI, utilizando el **protocolo IP** para dirigir paquetes de datos entre redes diferentes.

**Tablas de enrutamiento**: Almacenan información sobre rutas óptimas para enviar datos. Los protocolos de enrutamiento incluyen:

- **RIP (Routing Information Protocol)**: Protocolo simple basado en distancia.
- **OSPF (Open Shortest Path First)**: Protocolo avanzado que calcula rutas óptimas (nota: el documento escribe erróneamente "OPSF").
- **EIGRP (Enhanced Interior Gateway Protocol)**: Protocolo propietario de Cisco, eficiente para redes grandes (escrito como "Enhaced" en el documento, un error tipográfico).
- **BGP (Border Gateway Protocol)**: Usado en Internet para enrutamiento entre dominios.

### Comparación entre Hub, Switch y Router

El documento incluye una tabla comparativa:

|**Característica**|**Hub**|**Switch**|**Router**|
|---|---|---|---|
|**Capa OSI**|Capa 1 (Física)|Capa 2 (Enlace de Datos)|Capa 3 (Red)|
|**Inteligencia**|Ninguna, transmite a todos los puertos|Media, usa direcciones MAC|Alta, usa direcciones IP y tablas de enrutamiento|
|**Difusión del tráfico**|Envía a todos los puertos|Solo al puerto destino|Solo entre redes diferentes|
|**Dirección que maneja**|No maneja direcciones|Dirección MAC|Dirección IP|
|**Ideal para**|Redes pequeñas o antiguas|Redes modernas con alta demanda|Conectar LAN con WAN (Internet)|

### Tipos y funciones de los routers

- **Routers domésticos**: Usados en hogares para conectar dispositivos a Internet, con funciones básicas como NAT y DHCP.
- **Routers empresariales**: Diseñados para redes corporativas, con mayor capacidad y funciones avanzadas.
- **Routers de borde (Edge routers)**: Conectan redes internas con externas, como Internet.
- **Routers Core**: Gestionan el tráfico dentro de grandes redes, como en proveedores de servicios.

**Razones para usar routers**:

- Conectar redes locales (LAN) con redes externas (WAN).
- Gestionar tráfico eficiente entre múltiples redes.

### Funciones avanzadas de un router

- **NAT (Network Address Translation)**: Traduce direcciones IP públicas a privadas, permitiendo que múltiples dispositivos compartan una IP pública.
- **DHCP (Dynamic Host Configuration Protocol)**: Asigna direcciones IP automáticamente a dispositivos en la red.
- **Firewall básico**: Filtra el tráfico de red para mejorar la seguridad.
- **ACL (Access Control List)**: Controla el acceso a dispositivos o recursos específicos.
- **VPN (Virtual Private Network)**: Proporciona conexiones seguras y remotas mediante cifrado.

### Cómo elegir un router

El documento ofrece criterios para seleccionar un router adecuado:

- **Número de usuarios**:
    - Ejemplo: Un router con **700,000 sesiones TCP concurrentes** puede manejar entre **2,000 y 5,000 usuarios** (1 usuario ≈ 100–300 sesiones).
    - Para empresas con 50, 100 o 500 personas, se evalúa la capacidad según las sesiones.
- **Velocidad de Internet**:
    - Ejemplo: Un router que soporta **800 Mbps** con todas las funciones activadas (NAT, firewall, VPN).
- **Conexiones VPN**:
    - Ejemplo: Soporte para **200 usuarios SSL-VPN**, ideal para trabajo remoto.

### Ejercicio práctico: Introducción a routers con Packet Tracer

El documento incluye preguntas para un ejercicio con **Packet Tracer**, una herramienta de simulación de redes:

1. **Diferencias físicas entre router y switch**: Los routers tienen puertos WAN y capacidades de enrutamiento, mientras que los switches tienen más puertos Ethernet para conexiones locales.
2. **Conexión directa de un PC al router**: Sí, pero requiere configuración (como asignación de IP), ya que el router no actúa como switch sin ajustes.
3. **Función de un router sin configurar**: No enruta tráfico ni asigna IPs, quedando inactivo o limitado a funciones básicas.
4. **Comunicación entre PCs conectados a un switch**: No se comunican si no tienen IPs asignadas o si el switch no está conectado a un router para redes externas.
5. **Ubicación del router en una red grande**: Como puerta de enlace (gateway) entre la LAN y la WAN.
6. **Interfaces del router**: Se pregunta si las interfaces están disponibles y funcionan, pero no se especifican en el texto (probablemente ilustradas en imágenes).