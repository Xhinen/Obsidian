### 1. Dirección IPv4

**Definición**: IPv4 (Internet Protocol version 4) es un protocolo de la capa de red que utiliza direcciones de **32 bits**, divididas en **4 bloques de 8 bits** (un byte por bloque), representadas en formato decimal (ejemplo: 192.168.1.10).

**Conversión binario-decimal**:

- Cada bit en un byte representa un valor en potencias de 2 (128, 64, 32, 16, 8, 4, 2, 1).
- Ejemplo:
    - Binario: 10110010
    - Cálculo: <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mn>1</mn><mo>×</mo><mn>128</mn><mo>+</mo><mn>0</mn><mo>×</mo><mn>64</mn><mo>+</mo><mn>1</mn><mo>×</mo><mn>32</mn><mo>+</mo><mn>1</mn><mo>×</mo><mn>16</mn><mo>+</mo><mn>0</mn><mo>×</mo><mn>8</mn><mo>+</mo><mn>0</mn><mo>×</mo><mn>4</mn><mo>+</mo><mn>1</mn><mo>×</mo><mn>2</mn><mo>+</mo><mn>0</mn><mo>×</mo><mn>1</mn><mo>=</mo><mn>178</mn></mrow><annotation encoding="application/x-tex">1 \times 128 + 0 \times 64 + 1 \times 32 + 1 \times 16 + 0 \times 8 + 0 \times 4 + 1 \times 2 + 0 \times 1 = 178</annotation></semantics></math>1×128+0×64+1×32+1×16+0×8+0×4+1×2+0×1=178
    - Resultado: 178 en decimal.

**Clases fijas (A, B, C)**:

- **Clase A**:
    - Rango: 1.0.0.0 – 126.255.255.255
    - Máscara por defecto: 255.0.0.0 (/8)
    - Bits: 8 de red, 24 de host
    - Redes: 126 posibles
    - Hosts por red: 16,777,214
- **Clase B**:
    - Rango: 128.0.0.0 – 191.255.255.255
    - Máscara por defecto: 255.255.0.0 (/16)
    - Bits: 16 de red, 16 de host
    - Redes: 16,384 posibles
    - Hosts por red: 65,534
- **Clase C**:
    - Rango: 192.0.0.0 – 223.255.255.255
    - Máscara por defecto: 255.255.255.0 (/24)
    - Bits: 24 de red, 8 de host
    - Redes: 2,097,152 posibles
    - Hosts por red: 254

**Direcciones especiales**:

- **127.0.0.1**: Loopback/localhost, usado para pruebas internas.
- **127.x.x.x**: Reservado para pruebas.

### 2. Máscara de subred

**Definición**: La máscara de subred divide una dirección IP en **parte de red** y **parte de host**, permitiendo segmentar redes.

**Ejemplo**:

- Dirección IP: 192.168.1.10
- Máscara: 255.255.255.0 (/24)
- En binario:
    - IP: 11000000.10101000.00000001.00001010
    - Máscara: 11111111.11111111.11111111.00000000
- Resultado:
    - Los primeros 24 bits (1s) identifican la red.
    - Los últimos 8 bits (0s) identifican los hosts.

**Direcciones clave**:

- **192.168.1.0**: Dirección de red (no asignable a hosts).
- **192.168.1.1**: Primera IP útil.
- **192.168.1.254**: Última IP útil.
- **192.168.1.255**: Dirección de broadcast (para enviar datos a todos los dispositivos de la subred).

**CIDR (Classless Inter-Domain Routing)**:

- Sustituye las clases fijas, permitiendo máscaras variables.
- Ejemplos:
    - /8: 16,777,214 IPs (Clase A)
    - /16: 65,534 IPs (Clase B)
    - /24: 254 IPs (Clase C)
    - /26: 62 IPs (26 bits de red, 6 de host)
    - /30: 2 IPs (30 bits de red, 2 de host)

### 3. IPv6

**Definición**: IPv6 (Internet Protocol version 6) es el sucesor de IPv4, con direcciones de **128 bits** representadas en formato **hexadecimal**.

**Características**:

- Proporciona más de **340 undecillones** de direcciones, eliminando la escasez de IPv4.
- Usa **SLAAC (Stateless Address Autoconfiguration)** para configurar direcciones automáticamente.
- Soporta **DHCPv6** para asignación dinámica.
- Dirección loopback: ::1.

**Formato**:

- Completo: 2001:0db8:0000:0000:0000:ff00:0042:8329
- Abreviado: 2001:db8::ff00:42:8329 (eliminando ceros iniciales y secuencias de ceros).
- Prefijo: /64 (64 bits para la red).

**Tipos de direcciones**:

- **Link-local**: Configurada automáticamente, usada en la red local (ejemplo: fe80::1a2b:3c4d:5e6f:7890).
- **Global Unicast**: Configurada por SLAAC o manualmente, para redes globales (ejemplo: 2001:db8:abcd::10, red: 2001:db8:abcd::/64).
- **Default Gateway**: Generalmente una dirección link-local del router (ejemplo: fe80::1).

### 4. ARP (Address Resolution Protocol)

**Definición**: Protocolo que mapea una dirección **IP** a una dirección **MAC** en una red local.

**Funcionamiento**:

1. Un dispositivo (A) busca la MAC asociada a una IP en su caché ARP.
2. Si no la encuentra, envía un **ARP Request** en broadcast a la red.
3. El dispositivo con la IP solicitada (B) responde con un **ARP Reply** que incluye su MAC.
4. El dispositivo A almacena la MAC en su caché y usa esa dirección para enviar paquetes.

**Uso**: Esencial para la comunicación en LAN, ya que los switches operan con direcciones MAC.

### 5. RARP (Reverse Address Resolution Protocol)

**Definición**: Protocolo obsoleto que mapea una dirección **MAC** a una dirección **IP**, usado en dispositivos sin disco.

**Funcionamiento**:

1. Un dispositivo envía su MAC en un **RARP Request** en broadcast.
2. Un servidor RARP consulta una tabla estática (MAC → IP) y responde con la IP correspondiente.

**Limitaciones**: Sustituido por DHCP debido a su falta de flexibilidad y dependencia de tablas estáticas.

### 6. DHCP (Dynamic Host Configuration Protocol)

**Definición**: Protocolo que asigna automáticamente parámetros de red a dispositivos, incluyendo:

- Dirección IP.
- Máscara de subred.
- Puerta de enlace (gateway).
- Servidores DNS.
- Duración del "alquiler" de la IP.

**Proceso DORA**:

1. **Discover**: El cliente envía un mensaje en broadcast para localizar un servidor DHCP.
2. **Offer**: El servidor ofrece una IP y otros parámetros.
3. **Request**: El cliente acepta la oferta.
4. **Acknowledge**: El servidor confirma la asignación.

**Ventajas**: Simplifica la configuración de red, evita conflictos de IP y centraliza la gestión.

### 7. Red plana

**Definición**: Red donde todos los dispositivos (PCs, servidores, impresoras) están en la **misma subred**, sin VLANs ni segmentación.

**Ventajas**:

- **Sencillez**: Fácil de configurar y mantener, ideal para pequeñas empresas o redes pequeñas.
- **Bajo coste**: No requiere switches gestionables ni firewalls avanzados.
- **Comunicación rápida**: Sin latencia añadida por routers o VLANs.

**Problemas**:

- **Seguridad**: Un dispositivo comprometido puede afectar toda la red.
- **Tráfico de broadcast**: Puede causar congestión en redes grandes (ejemplo: ARP storms).
- **Sin control de acceso**: Cualquier usuario puede acceder a recursos sensibles.
- **Escalabilidad**: Inviable para redes con muchos dispositivos.

### 8. Modelo de tres capas

**Definición**: Diseño jerárquico para redes empresariales, dividido en tres niveles:

- **Capa de Acceso**: Conecta dispositivos finales (PCs, impresoras, puntos de acceso). Implementa VLANs, control de acceso (ACL, 802.1X) y seguridad.
- **Capa de Distribución**: Gestiona el enrutamiento entre VLANs (switches de capa 3), aplica políticas de red, filtrado y QoS (Calidad de Servicio).
- **Capa de Núcleo**: Proporciona alta velocidad y baja latencia para conectar la red interna.

**Ventajas**:

- **Escalabilidad**: Facilita la integración de nuevos dispositivos.
- **Mantenimiento modular**: Permite actualizaciones por capas.
- **Seguridad segmentada**: Controla accesos mediante VLANs y ACLs.
- **Redundancia**: Ofrece rutas alternativas ante fallos.

### 9. Diseño físico y lógico de una red jerárquica

**Topologías comunes**:

- **Estrella extendida**: Dispositivos conectados a un punto central con ramificaciones.
- **Árbol**: Organización jerárquica por capas.

**Diseño físico y lógico**:

- **Físico**: Incluye conexiones físicas y cableado estructurado.
- **Lógico**: Define el flujo de datos, VLANs y subredes.

**Conexiones clave**:

- **Uplink**: Conecta capas inferiores con superiores.
- **Trunk**: Transporta múltiples VLANs entre dispositivos.

**Cableado estructurado**:

- Organiza el cableado para facilitar el mantenimiento.
- Cumple normativas como TIA/EIA.

### 10. Buenas prácticas de diseño en redes jerárquicas

- Usar **VLANs** por departamentos o funciones (ejemplo: usuarios, servidores, voz).
- Separar tráfico para optimizar rendimiento.
- Evitar puntos únicos de fallo mediante redundancia física y lógica.
- Implementar protocolos como:
    - **STP (Spanning Tree Protocol)**: Evita bucles en la red.
    - **EtherChannel**: Agrupa enlaces para mayor ancho de banda y redundancia.

### 11. Ejercicios

El documento menciona ejercicios asociados a imágenes (image1.jpeg a image15.jpeg), pero no proporciona detalles. Es probable que incluyan tareas prácticas, como:

- Configuración de direcciones IP y máscaras de subred.
- Análisis de procesos DHCP o ARP.
- Diseño de redes planas o jerárquicas usando herramientas como Packet Tracer.