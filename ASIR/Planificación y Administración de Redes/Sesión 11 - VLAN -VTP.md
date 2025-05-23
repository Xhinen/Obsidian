### VLANs: Segmentación lógica de redes físicas

**Definición**: Las VLANs son redes lógicas creadas sobre una infraestructura física común, que agrupan dispositivos independientemente de su ubicación física.

**Beneficios**:

- **Aislamiento de tráfico**: Separa el tráfico entre grupos, mejorando la seguridad.
- **Mejora de rendimiento**: Reduce el tráfico innecesario y la congestión.
- **Optimización del ancho de banda**: Limita el tráfico de difusión (broadcast) a cada VLAN.

**Problemas sin VLANs**:

- **Tráfico innecesario**: Todos los dispositivos reciben datos irrelevantes.
- **Broadcast storms**: Tráfico de difusión excesivo que satura la red.
- **Vulnerabilidades de seguridad**: Falta de aislamiento facilita accesos no autorizados.

### Etiquetado de tráfico (Trunking)

**Definición**: Permite transportar tráfico de múltiples VLANs en un único enlace físico mediante el estándar **IEEE 802.1Q**, que agrega etiquetas a las tramas Ethernet para identificar la VLAN.

**Tipos de puertos**:

- **Access Ports**:
    - Pertenecen a una sola VLAN.
    - Usados para conectar dispositivos finales (PCs, impresoras).
    - Tráfico no etiquetado (untagged).
- **Trunk Ports**:
    - Transportan tráfico de múltiples VLANs.
    - Usados en enlaces entre switches o entre switches y routers.
    - Tráfico etiquetado (tagged) con IEEE 802.1Q.

### VLAN Trunking Protocol (VTP)

**Definición**: Protocolo de Cisco que distribuye automáticamente información de VLANs entre switches dentro de un mismo dominio VTP.

**Propósito**:

- Simplificar la administración de VLANs en redes grandes.
- Garantizar coherencia en la configuración de VLANs.

**Conexión**: Funciona sobre enlaces trunk, requiriendo que los switches estén en el mismo dominio VTP.

**Beneficios**:

- **Administración centralizada**: Configuración desde un único punto.
- **Ahorro de tiempo**: Reduce la configuración manual.
- **Coherencia**: Mantiene la misma configuración de VLANs en toda la red.
- **Reducción de errores humanos**: Automatiza la propagación de cambios.

### Modos de VTP

1. **VTP Server**:
    - Crea, modifica y elimina VLANs.
    - Propaga información de VLANs a otros switches del dominio.
    - Guarda la configuración en **NVRAM** (memoria no volátil).
    - Actúa como el centro de administración de VLANs.
2. **VTP Client**:
    - No puede crear ni modificar VLANs.
    - Recibe y aplica cambios desde un VTP Server.
    - No guarda la configuración tras reinicio (depende del servidor).
3. **VTP Transparent**:
    - No participa en la base de datos VTP.
    - No propaga ni aplica cambios VTP, pero reenvía mensajes VTP.
    - Puede administrar VLANs localmente.

**Tabla comparativa**:

| **Funcionalidad**              | **Server** | **Client** | **Transparent** |
| ------------------------------ | ---------- | ---------- | --------------- |
| Crear/modificar/eliminar VLANs | ✅          | ❌          | ✅ (solo local)  |
| Propagar información de VLANs  | ✅          | ✅          | ❌               |
| Recibir información VTP        | ✅          | ✅          | ❌               |
| Reenviar tramas VTP            | ✅          | ✅          | ✅               |
| Guarda configuración (NVRAM)   | ✅          | ❌          | ✅               |

### Dominios VTP y versiones

**Dominio VTP**:

- Nombre común que deben compartir todos los switches para intercambiar información de VLANs.
- **Requisito**: Si el nombre de dominio no coincide, los anuncios VTP son ignorados.
- **Contraseña VTP (opcional)**: Aumenta la seguridad, permitiendo la propagación solo entre switches con la misma clave.

**Versiones VTP**:

- **VTPv1**: Soporta VLANs estándar (1–1005).
- **VTPv2**: Mejora compatibilidad con Token Ring.
- **VTPv3**: Soporta VLANs extendidas (1006–4094) y seguridad avanzada.

**Revision Number**:

- Número que aumenta con cada modificación de VLAN.
- Un switch con un número de revisión alto (incluso sin VLANs) puede sobrescribir la configuración de toda la red, causando problemas si no se gestiona correctamente.

**Tabla comparativa de versiones**:

|**Característica**|**VTPv1**|**VTPv2**|**VTPv3**|
|---|---|---|---|
|Soporte para VLANs extendidas (>1005)|❌|❌|✅ (1006–4094)|
|Autenticación de contraseñas|❌|❌|✅|
|Modo Transparent|❌|❌|✅ (reenvía tramas VTP)|
|Propagación de VLANs|Solo Server/Client|Solo Server/Client|Server/Client/Transparent|
|Compatibilidad hacia atrás|❌|✅ (con VTPv1)|✅ (con VTPv1 y VTPv2)|
|Manejo de VLANs|Solo en servidor|Solo en servidor|Servidor y Transparent|
|Número de revisión|Sistema básico|Sistema básico|Mejora gestión para evitar sobrescrituras|
|Seguridad|Sin mecanismos|Sin mecanismos|Contraseñas y autenticación|
|Actualización del dominio VTP|Requiere servidor|Algunas actualizaciones|Actualización más segura|
|Difusión de VLANs|Sin filtrado|Sin filtrado|Permite filtrado de VLANs|

### Funcionamiento del protocolo VTP

**Tráfico VTP**:

- Se transmite a través de **enlaces trunk**.
- Requiere que el **Cisco Discovery Protocol (CDP)** esté activo para facilitar la comunicación entre switches.

**Paquetes VTP**:

- **Tipos de mensaje**:
    - **Summary Advertisement**: Resumen de cambios.
    - **Subset Advertisement**: Detalles de VLANs específicas.
    - **Request**: Solicitud de información por parte de clientes.
- Incluyen:
    - Nombre de dominio VTP.
    - Número de revisión.
    - Lista de VLANs.

**Flujo de sincronización**:

1. Un **VTP Server** realiza cambios en las VLANs.
2. Envía un **Summary Advertisement** a otros switches.
3. Los **VTP Clients** responden con un **Request** si necesitan detalles.
4. El servidor envía un **Subset Advertisement** con la información completa.