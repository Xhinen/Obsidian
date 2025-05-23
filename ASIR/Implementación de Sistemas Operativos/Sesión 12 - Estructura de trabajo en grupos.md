### 1. Estructura Cliente-Servidor

**Definición**: La arquitectura cliente-servidor es un modelo de red donde:

- El **cliente** realiza peticiones de servicios o recursos (por ejemplo, abrir una página web).
- El **servidor** responde proporcionando el servicio o recurso solicitado (por ejemplo, enviar el contenido HTML de la web). La comunicación se realiza mediante **protocolos de red** como HTTP, FTP, SSH, entre otros.

**Ejemplos de cliente-servidor y protocolos** (presentados como posible pregunta de examen):

- Navegador web (cliente) ↔ Servidor Apache/Nginx (servidor) → Protocolo HTTP/HTTPS.
- FileZilla (cliente) ↔ Servidor vsFTPd (servidor) → Protocolo FTP/SFTP.
- Cliente de correo ↔ Servidor de correo → Protocolo IMAP/SMTP.
- Terminal SSH ↔ Servidor OpenSSH → Protocolo SSH.
- Resolución de dominio ↔ Servidor DNS (BIND) → Protocolo DNS.

**Funciones como administradores**:

- Configurar servicios de red (servidores web, DNS, DHCP, bases de datos, etc.).
- Detectar errores de comunicación entre cliente y servidor.
- Diseñar infraestructuras seguras y eficientes.
- Automatizar la administración mediante scripts y herramientas.

### 2. Protocolo LDAP

**Definición**: El **Lightweight Directory Access Protocol (LDAP)** es un protocolo de red que permite acceder, consultar y modificar servicios de directorio distribuidos a través de TCP/IP. Un directorio LDAP es una base de datos optimizada para lectura, con información estructurada y jerárquica, como:

- Cuentas de usuario.
- Grupos.
- Equipos.
- Permisos y políticas.

**Usos de LDAP**:

- Autenticación de usuarios en redes corporativas.
- Integración con servicios como Samba, Apache, OpenVPN, etc.
- Gestión de identidades.
- Implementación de Single Sign-On (SSO).

**Estructura de un directorio LDAP** (ejemplo):

- Dominio raíz: dc=Colegios,dc=local.
- Unidades organizativas: ou=usuarios (con usuarios como uid=juan, uid=ana) y ou=grupos (con grupos como cn=Profesores, cn=alumnos).
- Componentes:
    - dc: Domain Component (dominio).
    - ou: Organizational Unit (unidad organizativa).
    - uid: User ID (identificador de usuario).
    - cn: Common Name (nombre del grupo).

**Limitaciones y complementos**:

- LDAP no gestiona directamente contraseñas ni políticas de seguridad avanzadas, pero se combina con servicios como **Kerberos**.
- Aplicaciones:
    - Sistemas Linux (usando PAM + NSS + LDAP).
    - Servidores web (Apache + LDAP).
    - Correo electrónico (Postfix, Dovecot).
    - Samba para compartir archivos en red.

**Kerberos**:

- Protocolo de autenticación de red desarrollado por el MIT (proyecto Athena).
- Características:
    - **Autenticación mutua**: Cliente y servidor se autentican mutuamente.
    - Evita enviar contraseñas por la red, usando cifrado y "tickets".
    - Basado en criptografía de clave simétrica.
    - Utiliza claves temporales y tickets para acceder a servicios.
- Ampliamente usado en entornos corporativos y educativos.

### 3. Concepto de dominio, subdominios y requisitos para su montaje

**Dominio**:

- Un dominio en Windows es un entorno de red gestionado centralmente mediante **Active Directory Domain Services (AD DS)**.
- Características:
    - Centralización de la gestión de usuarios, equipos y políticas.
    - Autenticación mediante Single Sign-On (SSO).
    - Aplicación de **políticas de grupo (GPO)**.
    - Control de acceso a recursos (archivos, impresoras, etc.).

**Subdominios**:

- Divisiones lógicas de un dominio principal, útiles para:
    - Delegación de administración.
    - Separación geográfica o por departamentos.
    - Reducción del tráfico de replicación.
- Ejemplo:
    - Dominio raíz: ventanas.local.
    - Subdominios: madrid.ventanas.local, sevilla.ventanas.local.

**Requisitos para montar un dominio**:

1. **Hardware y software**:
    - Servidor con Windows Server (2016, 2019 o 2022).
    - Mínimo 4 GB de RAM (preferiblemente más).
    - Al menos 40 GB de espacio libre en disco.
    - Nombre del equipo correctamente definido.
2. **Configuración de red**:
    - Dirección IP estática.
    - Nombre DNS completo (FQDN), por ejemplo, asignaturas.local.
    - Conectividad entre clientes y servidor (switches, AP, routers).
3. **Instalación del rol de Active Directory**:
    - Instalar el rol "Servicios de dominio de Active Directory (AD DS)".
    - Promover el servidor como Controlador de Dominio (DC).
    - Crear el dominio (ejemplo: asignaturas.local).
4. **Estructura de AD**:
    - Crear **unidades organizativas (OU)** para organizar usuarios, equipos y grupos.
    - Añadir usuarios y equipos al dominio.
    - Aplicar políticas de grupo (GPO) según las necesidades del entorno.