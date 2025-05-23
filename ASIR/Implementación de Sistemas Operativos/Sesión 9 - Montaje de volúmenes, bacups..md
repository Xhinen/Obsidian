### 1. Montaje de volúmenes en carpetas

Se define como la organización del almacenamiento físico en áreas lógicas para facilitar la gestión y acceso a archivos. Se destacan dos ejemplos prácticos:

- **Almacenamiento NAS (Network Attached Storage)**: Configuración de carpetas compartidas vinculadas a un Active Directory (AD) para acceso centralizado.
- **Carpeta compartida local**: Un disco duro dedicado para datos de un servidor, accesible por un grupo de usuarios locales, con opciones de permisos personalizados.

Se menciona una interfaz de configuración (en español) para establecer permisos avanzados, compartir recursos y proteger carpetas con credenciales.

### 2. Tolerancia a fallos de software de los datos

Esta sección explica cómo los sistemas incorporan características para mantener el funcionamiento tras fallos en componentes. Se destacan:

- **Desventajas**: Reducción en el nivel de producción y mayores tiempos de respuesta.
- **Estrategias de tolerancia a fallos**:
    - **Hardware**: Uso de servidores idénticos en paralelo, replicando operaciones en un servidor de respaldo.
    - **Software**: Replicación continua de bases de datos en otra máquina, permitiendo redirigir operaciones si la principal falla.
    - **Fuentes de energía**: Uso de generadores alternativos para garantizar continuidad en caso de fallos eléctricos.

### 3. Tipos de copias de seguridad

Se describen las copias de seguridad como una medida para proteger datos en dispositivos (ordenadores, tablets, etc.), almacenándolos en discos externos o servicios en la nube. Los tipos se clasifican según:

- **Ejecución**: Automáticas o manuales.
- **Contenido**:
    - **Completas**: Copian todos los datos, requieren más espacio y tiempo, suelen realizarse fuera del horario laboral y tienen un coste elevado.
    - **Diferenciales**: Copian archivos modificados o nuevos desde la última copia completa. Menos espacio que las completas, pero no optimizan tanto el tiempo ni el espacio.
    - **Incrementales**: Copian solo los datos modificados desde la última copia (de cualquier tipo), optimizando espacio y tiempo gracias al registro de fechas y horas por aplicaciones de backup.
    - **En espejo**: No se detalla en el documento, pero se menciona como tipo.

### 4. Planes de copias de seguridad y programación

Aunque el documento no profundiza, se infiere que esta sección aborda la importancia de establecer estrategias y horarios para realizar copias de seguridad, optimizando recursos y minimizando interrupciones.

### 5. Recuperación en caso de fallo del sistema

Se describe la capacidad de revertir el estado de un sistema a un punto anterior mediante puntos de restauración. Esto es útil para solucionar problemas causados por:

- Instalaciones de software.
- Actualizaciones de controladores.
- Cambios en la configuración del sistema.

Se detalla una interfaz de "Restaurar sistema" que permite seleccionar un punto de restauración (ejemplo: 28/04/2025, tras un Windows Update) y advierte sobre la necesidad de reiniciar el equipo, guardar archivos abiertos y, en caso de cambio reciente de contraseña, crear un disco de restablecimiento.

### 6. Enlaces de interés

El documento incluye dos recursos adicionales:

- Guía sobre copias de seguridad del INCIBE: [https://www.incibe.es/ciudadania/tematicas/copias-seguridad](https://www.incibe.es/ciudadania/tematicas/copias-seguridad)
- Tutorial sobre RAID en discos duros: [https://hardzone.es/tutoriales/montaje/raid-discos-duros/](https://hardzone.es/tutoriales/montaje/raid-discos-duros/)