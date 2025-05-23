### LAN (Local Area Network) y WAN (Wide Area Network)

**LAN**:

- **Definición**: Red de área local limitada a un área pequeña, como un edificio.
- **Características**:
    - Usa tecnologías como **Ethernet** y **Wi-Fi**.
    - Ofrece **alta velocidad** y **baja latencia**.
    - Generalmente de **propiedad privada**.
- **Propósito**: Conectar dispositivos cercanos para compartir recursos (archivos, impresoras).

**WAN**:

- **Definición**: Red de área amplia que cubre grandes distancias, como ciudades o países.
- **Características**:
    - Usa tecnologías como **fibra óptica**, **satélites** y **microondas**.
    - Velocidades y latencia **variables** según la tecnología.
    - Gestionada por **proveedores de servicios de Internet (ISP)**.
- **Propósito**: Conectar LANs distantes para comunicación global.

### Componentes de una red WAN

- **CPE (Customer Premises Equipment)**: Dispositivos en las instalaciones del cliente, como routers o módems, que conectan la LAN al proveedor.
- **DTE (Data Terminal Equipment)**: Dispositivos que generan o consumen datos, como servidores o PCs.
- **DCE (Data Communication Equipment)**: Equipos que facilitan la transmisión de datos, como módems o multiplexores.
- **Proveedor de Servicios (ISP)**: Proporciona la infraestructura de red (fibra, satélite) para conectar LANs.

### RDSI (Red Digital de Servicios Integrados)

**Definición**: Tecnología que integra voz y datos en una red digital a través de líneas telefónicas.

**Características**:

- **Canales**:
    - **Canal B**: 64 Kbps para transmisión de datos y voz.
    - **Canal D**: Usado para señalización y control.
- **Arquitectura**: Combina voz y datos en una única red digital.
- **NT1 (Network Termination 1)**: Dispositivo que conecta la red RDSI con los equipos locales.
- **Adaptadores RDSI**: Permiten conectar equipos estándar a la red digital.

**Velocidad**: Hasta 128 Kbps.

### Frame Relay

**Definición**: Tecnología de conmutación de paquetes para redes WAN, basada en circuitos virtuales.

**Características**:

- **Circuitos virtuales**:
    - **PVC (Permanent Virtual Circuit)**: Conexión fija.
    - **SVC (Switched Virtual Circuit)**: Conexión temporal.
- **DLCI (Data Link Connection Identifier)**: Identificador para circuitos virtuales.
- **Alta eficiencia**: Baja corrección de errores para maximizar velocidad.
- **Sustitución**: Reemplazada por tecnologías modernas como **MPLS** y **VPN**.
- **Velocidad**: 56 Kbps a 1.5 Mbps.

**Gestión de la red**:

- **Control de congestión**:
    - **FECN (Forward Explicit Congestion Notification)**: Notifica congestión al receptor.
    - **BECN (Backward Explicit Congestion Notification)**: Notifica congestión al emisor.
- **Topologías**: Estrella o malla parcial en redes empresariales.
- **Ventajas**: Bajo coste, alta velocidad, topologías flexibles.
- **Limitación**: Dependiente de la calidad de la línea.

### ADSL (Asymmetric Digital Subscriber Line)

**Definición**: Tecnología que utiliza líneas telefónicas tradicionales para transmitir datos, con velocidades asimétricas (mayor velocidad de descarga que de subida).

**Características**:

- **Velocidad**:
    - Descarga: 1 Mbps a 24 Mbps.
    - Subida: Menor que la descarga.
- **Dependencia**: La velocidad disminuye con la distancia a la central telefónica (máximo ~5 km).
- **Componentes**:
    - **Splitter**: Separa la señal telefónica de los datos.
    - **Módem ADSL y router**: Convierten y dirigen la señal.
- **Multiplexación**:
    - Usa **FDM (Frequency Division Multiplexing)**.
    - Frecuencias bajas (0 Hz a 4 kHz): Voz.
    - Frecuencias altas (138 kHz a 1.1 MHz): Datos.
- **Comparación**:
    - **Cable coaxial**: Mayor velocidad, pero compartida entre usuarios.
    - **Fibra óptica**: Mayor capacidad, sin pérdida por distancia.

### Tecnologías posteriores

1. **Cable Módem (DOCSIS)**:
    - Usa cable coaxial (como el de TV por cable).
    - Velocidad compartida entre usuarios.
    - Mejor velocidad de descarga que de subida.
2. **Fibra Óptica (FTTH - Fiber to the Home)**:
    - Usa señales ópticas (luz) para transmisión de datos.
    - **Velocidad simétrica**: Igual en descarga y subida.
    - **Sin pérdida por distancia**.
    - Tipos:
        - **Fibra multimodo**: Para distancias cortas.
        - **Fibra monomodo**: Para largas distancias.
    - Velocidad: 100 Mbps a 1 Gbps o más.
3. **Redes móviles (3G, 4G, 5G)**:
    - Evolución de 3G (navegación básica) a 5G (ultra baja latencia).
    - Usos: Dispositivos móviles, IoT, ciudades inteligentes.
    - Velocidad:
        - 4G: 20–100 Mbps.
        - 5G: 100 Mbps–1 Gbps+.
4. **WISP (Wireless Internet Service Provider)**:
    - Conexión inalámbrica mediante antenas de radiofrecuencia.
    - Requiere línea de vista con la antena del proveedor.
5. **Internet satelital moderno (ejemplo: Starlink)**:
    - Usa satélites en órbita baja para baja latencia.
    - Ideal para zonas rurales o remotas.
    - Velocidad: 50–250 Mbps.
    - Latencia: 25–50 ms.
    - Enlace: [https://www.starlink.com/es/map](https://www.starlink.com/es/map).

### Resumen comparativo

El documento incluye una tabla que compara las tecnologías WAN:

|**Tecnología**|**Descripción**|**Velocidad aproximada**|
|---|---|---|
|**RDSI (ISDN)**|Red digital que transmite voz y datos simultáneamente.|Hasta 128 Kbps|
|**Frame Relay**|Transmisión de datos en redes WAN orientada a paquetes.|56 Kbps a 1.5 Mbps|
|**ADSL**|Línea telefónica con división de frecuencias para voz y datos.|1 Mbps a 24 Mbps (descarga)|
|**FTTH**|Fibra óptica directa al hogar, alta velocidad y baja latencia.|100 Mbps a 1 Gbps o más|
|**Red móvil (4G/5G)**|Internet vía red celular. 5G ofrece mayor velocidad y menor latencia.|4G: 20–100 Mbps / 5G: 100 Mbps–1 Gbps+|
|**Red satelital**|Internet desde satélites, útil en zonas rurales.|50–250 Mbps, latencia 25–50 ms|
|**WISP**|Proveedor inalámbrico por antenas de radiofrecuencia.|Variable|