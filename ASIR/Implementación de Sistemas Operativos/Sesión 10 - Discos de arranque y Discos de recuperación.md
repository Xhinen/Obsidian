### 1. Discos de arranque y discos de recuperación

Se define un **disco de arranque** como un dispositivo de almacenamiento desmontable que permite a un ordenador ejecutar un programa al encenderse. Sus usos incluyen:

- Recuperar archivos.
- Solucionar problemas de hardware y software.
- Probar programas.
- Instalar sistemas operativos.

Se destaca el uso del software **Rufus** para crear dispositivos USB de arranque, con un ejemplo práctico que muestra la configuración para crear un disco USB con Windows 11 (versión 22H2, build 22621.525, edición Home/Pro/Edu, en inglés internacional, con partición MBR y sistema de archivos FAT32). La interfaz de Rufus permite seleccionar la imagen ISO y personalizar parámetros como el volumen y la arquitectura.

### 2. Copias de seguridad del sistema y recuperación mediante consola

Esta sección detalla cómo realizar copias de seguridad y recuperar sistemas operativos, con énfasis en Windows 10 y 11:

- **Copias de seguridad en Windows 11**: Se pueden gestionar desde la configuración de cuentas, utilizando **OneDrive** para respaldar carpetas como Documentos, Imágenes, Escritorio, Música y Videos. La interfaz permite seleccionar qué carpetas respaldar y muestra el espacio disponible (ejemplo: 0.1 GB de 5 GB usados).
- **Recuperación mediante consola en Windows 10**: Se describe un procedimiento para restaurar el sistema desde el **Modo Seguro con Símbolo del Sistema**:
    1. Reiniciar el equipo manteniendo pulsada la tecla "Mayúsculas", seleccionar "Encendido" > "Reiniciar".
    2. En la pantalla de "Elegir una opción", ir a "Solucionar problemas" > "Opciones avanzadas" > "Configuración de inicio" > "Reiniciar".
    3. Seleccionar la opción 6 (Modo Seguro con Símbolo del Sistema).
    4. En la ventana CMD, ejecutar el comando rstrui.exe para iniciar el proceso de restauración, eligiendo entre un punto de restauración recomendado o uno específico.
- **Opciones de recuperación avanzadas**: Incluyen Modo Seguro, Modo Seguro con funciones de red, Modo de restauración de servicios de directorio, deshabilitar reinicio automático, entre otros, para reparar problemas de inicio.

### 3. Puntos de recuperación

Se menciona brevemente que este tema ya fue abordado en profundidad en sesiones anteriores, haciendo referencia a las "Propiedades del sistema" para gestionar puntos de restauración, aunque no se proporcionan detalles adicionales en esta sección.

### 4. Creación y recuperación de imágenes de servidores

Se explica que la creación de imágenes de servidores consiste en generar copias exactas del sistema para recuperación o replicación en caso de fallos. Se mencionan:

- **Snapshots**: Instantáneas del servidor que capturan su estado en un momento específico.
- **Herramientas**: Se pueden usar herramientas integradas como **Windows Backup** o soluciones de terceros como **Acronis** para crear y restaurar estas imágenes.

### 5. Cuotas de disco y niveles de advertencia

Las **cuotas de disco** son límites de almacenamiento establecidos para usuarios o grupos en un sistema operativo, con el objetivo de controlar el uso del espacio y evitar problemas de rendimiento. Se distinguen dos tipos:

- **Cuota dura**: Impide que el usuario utilice más espacio una vez alcanzado el límite.
- **Cuota blanda**: Permite exceder el límite temporalmente, generando alertas para el usuario y el administrador.

**Beneficios** de las cuotas de disco:

- Control del uso de espacio.
- Prevención de problemas de rendimiento.
- Aplicación de políticas de almacenamiento.

Se menciona que las alertas pueden dirigirse tanto al usuario como al administrador, ayudando a mantener un uso eficiente del disco.