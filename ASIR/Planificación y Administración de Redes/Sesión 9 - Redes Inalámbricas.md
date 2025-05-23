### WiFi (IEEE 802.11)

**Definición**: Tecnología de red inalámbrica de corto alcance utilizada en hogares, oficinas y espacios públicos.

**Estándar IEEE 802.11**:

- Define las comunicaciones para redes LAN inalámbricas.
- Organiza:
    - **Capa física**: Transmisión mediante ondas de radio.
    - **Capa de enlace de datos (MAC)**: Gestión de acceso al medio.
- **Evolución de estándares**:
    - **802.11b/g/n/ac/ax**: Mejoras progresivas en velocidad, eficiencia y alcance.

**IEEE 802.1X** (nota: el documento parece referirse erróneamente a 802.11 en esta sección):

- **Definición**: Estándar para controlar el acceso a la red por cada conexión ("puerto").
- **Componentes**:
    - **Suplicante**: Dispositivo que solicita acceso, usando **EAP** (Extensible Authentication Protocol) para identificarse.
    - **Autenticador**: Punto de acceso WiFi o switch que solicita identificación y se comunica con el servidor mediante **RADIUS** (Remote Authentication Dial-In User Service).
    - **Servidor**: Verifica identidades de los dispositivos.
- **Beneficio**: Garantiza que solo usuarios autorizados accedan a la red.

**Funcionamiento y seguridad en WiFi**:

- **Bandas de frecuencia**:
    - **2.4 GHz**: Mayor alcance, pero más interferencias.
    - **5 GHz**: Mayor velocidad, menos saturación.
- **Modos de funcionamiento**:
    - **Infraestructura**: Conexión mediante un router o punto de acceso (AP).
    - **Ad-hoc**: Conexión directa entre dispositivos sin punto de acceso.
- **Seguridad**:
    - **WEP**: Obsoleto, vulnerable.
    - **WPA/WPA2/WPA3**: Mejoras progresivas en cifrado y autenticación.
- **Configuraciones básicas**:
    - **SSID**: Nombre de la red.
    - **Canal**: Frecuencia específica para evitar interferencias.
    - **Tipo de cifrado**: WPA2/WPA3 recomendado.
    - **Filtrado MAC**: Restringe acceso a direcciones MAC específicas.
    - **QoS (Quality of Service)**: Prioriza tráfico para optimizar rendimiento.

### WiMAX

**Definición**: Tecnología de acceso inalámbrico de largo alcance, diseñada para redes metropolitanas o rurales.

**Características**:

- **Cobertura**: Hasta 50 km.
- **Velocidad**: Comparable a ADSL o fibra básica.
- **Escalabilidad**: Soporta desde pocos hasta miles de usuarios.
- **Estructura**: Usa antenas potentes, torres base y modulación **OFDM** (Orthogonal Frequency Division Multiplexing).
- **Bandas de frecuencia**: 2.3 GHz, 2.5 GHz, 3.5 GHz, 5.8 GHz.

**WiMAX vs WiFi**:

- **WiMAX**: Redes metropolitanas o rurales, mayor cobertura.
- **WiFi**: Redes locales (hogares, oficinas), menor alcance.

**Factores que afectan WiMAX**:

- Distancia a la torre base.
- Obstáculos físicos (edificios, árboles).
- Condiciones climáticas.
- Número de usuarios conectados.

**Propósito**:

- Proporcionar conectividad en áreas donde WiFi no es viable.
- Complementar, no reemplazar, WiFi.

### Evolución de las redes móviles

1. **1G (1979 - años 90)**:
    - **Definición**: Primera generación de comunicación móvil analógica.
    - **Características**:
        - Solo soportaba llamadas de voz.
        - Poca cobertura y baja calidad de llamada.
        - Sin soporte para datos.
    - **Multiplexación**: **FDMA** (Frequency Division Multiple Access).
2. **2G (GSM) y 2.5G (GPRS, EDGE)**:
    - **2G (1991 - 2000)**:
        - Introdujo voz digital mediante **GSM** (Global System for Mobile Communications).
        - **Características**:
            - SMS (mensajes de texto).
            - Mejor calidad de llamada.
            - Mayor seguridad que 1G.
        - **Multiplexación**: **TDMA** (Time Division Multiple Access).
    - **2.5G (1999 - 2003)**:
        - **GPRS**: Conexión a Internet móvil básica mediante conmutación de paquetes.
        - **EDGE**: Mejora en velocidades (~200 Kbps).
        - **Uso**: Primera experiencia real de datos móviles.
3. **3G (UMTS) y 3.5G (HSDPA)**:
    - **3G - UMTS (2001 - 2010)**:
        - **Definición**: Universal Mobile Telecommunications System, inicio del Internet móvil real.
        - **Características**:
            - Velocidades de hasta 2 Mbps.
            - **Arquitectura**: UTRAN (Node B + RNC) + Core Network.
            - Soporte para navegación y servicios básicos.
    - **3.5G - HSDPA (2005 - 2012)**:
        - **Definición**: High-Speed Downlink Packet Access.
        - **Características**:
            - Velocidades de hasta 14 Mbps (teóricos).
            - Mejoras técnicas: Modulación adaptativa, corrección de errores en Node B.
            - Mejora en servicios de datos.
4. **4G - LTE (Long Term Evolution)**:
    - **Características**:
        - Velocidades: Hasta 100 Mbps en movimiento, 1 Gbps en estático.
        - Latencia: 30-50 ms.
        - **Modulación**: **OFDMA** (enlace descendente) y **SC-FDMA** (enlace ascendente).
        - **MIMO**: Mejora la capacidad y rendimiento.
        - **Arquitectura**: All-IP para voz, datos y vídeo.
        - **Ancho de banda**: 20 MHz para mayor capacidad.
5. **5G**:
    - **Características**:
        - Velocidades: Hasta 20 Gbps.
        - Latencia: 1-10 ms (ultra baja).
        - Uso de **ondas milimétricas (mmWave)** para altas velocidades.
        - **Massive MIMO**: Cientos de antenas para mayor capacidad.
        - **Edge computing** y **virtualización** para baja latencia.
        - Soporte para millones de dispositivos IoT.
    - **Despliegue**:
        - **NSA (Non-Standalone)**: Usa infraestructura 4G.
        - **SA (Standalone)**: Red 5G independiente.