### 1. Servicio de ficheros distribuidos (DFS)

**Definición**: Un sistema de ficheros distribuidos (DFS) es un esquema de almacenamiento y gestión de datos que permite a usuarios y aplicaciones acceder a archivos (PDF, documentos de Word, imágenes, videos, audios, etc.) almacenados en múltiples servidores en red, desde un almacenamiento compartido.

**Razones para su uso**:

- Almacenar datos de forma permanente en dispositivos de almacenamiento secundario.
- Facilitar el intercambio de información entre usuarios y aplicaciones de manera eficiente y segura.

**Componentes críticos**:

- **Transparencia de ubicación**: Los usuarios ven un único espacio de nombres para todos los archivos, independientemente del servidor donde estén almacenados, y pueden mover archivos sin cambiar la ruta de acceso.
- **Redundancia**: Mediante la replicación de archivos, DFS distribuye copias a través de los nodos del clúster, garantizando alta disponibilidad incluso si un servidor falla.

**Características**:

- **Transparencia de acceso**: Los usuarios acceden a los archivos como si estuvieran en su dispositivo local.
- **Bloqueo de archivos**: Evita modificaciones simultáneas en el mismo archivo desde diferentes ubicaciones.
- **Cifrado de datos en tránsito**: Protege los datos mientras se mueven por el sistema.
- **Compatibilidad con múltiples protocolos**: Soporta protocolos como SMB, NFS y POSIX.

**Ventajas**:

- Acceso a datos desde múltiples ubicaciones.
- Intercambio eficiente de información a nivel global.
- **Resiliencia**: La replicación asegura que un fallo en un servidor no cause pérdida de datos.
- **Eficiencia de red**: Distribuye cargas de trabajo para evitar ralentizaciones.
- **Acceso inmediato a cambios**: Los cambios en archivos son visibles instantáneamente.
- **Escalabilidad**: Añadir nodos aumenta la capacidad del sistema.
- **Alta fiabilidad**: La replicación reduce el riesgo de pérdida de datos.

### 2. Encriptación de datos

**Definición**: La encriptación transforma información legible (texto claro) en texto cifrado para protegerla durante su almacenamiento o transmisión, garantizando confidencialidad, integridad y privacidad.

**Importancia**:

- Protege datos sensibles en sistemas, redes y bases de datos.
- Previene accesos no autorizados, intercepción de datos y alteraciones.

**Tipos de amenazas**:

- Acceso no autorizado (ataques de hackers).
- Intercepción de datos en redes inseguras.
- Alteración o corrupción de datos.

**Tipos de encriptación**:

- **Simétrica**: Usa una única clave para encriptar y desencriptar (ejemplos: AES, DES, RC4).
    - **Ventaja**: Rápida y eficiente.
    - **Desventaja**: La gestión segura de claves es un desafío en redes no confiables.
    - **Algoritmos**:
        - **AES (Advanced Encryption Standard)**: Estándar moderno, seguro y eficiente.
        - **DES (Data Encryption Standard)**: Obsoleto por vulnerabilidad a ataques de fuerza bruta.
        - **RC4**: Usado en SSL/TLS, pero obsoleto por debilidades.
- **Asimétrica**: Usa un par de claves (pública para encriptar, privada para desencriptar; ejemplos: RSA, ElGamal, ECC).
    - **Algoritmos**:
        - **RSA**: Basado en la factorización de números primos.
        - **ElGamal**: Usado en PGP para correo electrónico.
        - **ECC (Curvas Elípticas)**: Eficiente en seguridad por bit, usado en aplicaciones modernas.
    - **Certificados digitales y PKI**: Garantizan la autenticidad de claves públicas y gestionan su distribución.
    - **Firma digital**: Usa criptografía asimétrica para verificar la autenticidad de mensajes.

**Protocolos criptográficos**:

- **SSL/TLS**: Asegura comunicaciones web mediante autenticación y claves compartidas.
- **IPsec**: Cifra paquetes IP para VPNs.
- **PGP/GPG**: Protocolos para encriptar y autenticar correos electrónicos.
- **VPN**: Usa criptografía para conexiones privadas en redes públicas.

### 3. Compresión de datos

**Definición**: Proceso de reducir el tamaño de archivos o datos para optimizar almacenamiento y transmisión, manteniendo la integridad de la información.

**Importancia**:

- **Eficiencia en almacenamiento**: Permite guardar más datos en menos espacio.
- **Optimización de transmisión**: Reduce el tiempo de envío en redes, especialmente lentas.
- **Reducción de costos**: Menor uso de almacenamiento y ancho de banda.
- **Facilidad en respaldos**: Mejora la eficiencia en copias de seguridad.

**Tipos de compresión**:

- **Sin pérdida (Lossless)**: Permite recuperar los datos originales sin alteraciones.
    - **Formatos y aplicaciones**: .zip, .tar.gz, código fuente, bases de datos.
- **Con pérdida (Lossy)**: Descarta datos para reducir tamaño, lo que puede afectar la calidad.
    - **Formatos y aplicaciones**: JPEG, MP3, transmisiones de YouTube o Netflix.
    - **Ventaja**: Alta reducción de tamaño.
    - **Desventaja**: Pérdida de calidad, dependiendo del nivel de compresión.