### 🔌 1. Montaje y Desmontaje de Dispositivos

- **Montaje:** proceso que permite que archivos, directorios o dispositivos estén accesibles en el sistema.
    
    - **En Windows:** se gestiona desde Configuración > Dispositivos.
        
    - **En Linux:** si no se detecta automáticamente, se usa el comando `mount` en terminal.
        
- **Desmontaje:** desactiva el acceso al dispositivo.
    
    - **En Windows:** se realiza mediante clic derecho > "Expulsar".
        
    - **En Linux:** también con `umount` en terminal, aunque el documento repite `mount`, lo que puede ser un error.
        

---

### ⚙️ 2. Automatización de Tareas

- **Linux:**
    
    - `at`: ejecuta tareas únicas programadas.
        
    - `cron`: ejecuta tareas recurrentes, configuradas en el archivo `crontab`.
        

Estas herramientas permiten mantener procesos automatizados de mantenimiento o monitoreo.

---

### 💽 3. Herramientas de Administración de Discos

#### ➤ Tipos de Particiones

- **Primaria:** necesarias para instalar sistemas operativos.
    
- **Extendida:** permite superar el límite de 4 particiones primarias, solo almacena datos.
    
- **Lógica:** creadas dentro de una extendida, usadas para datos como si fueran discos independientes.
    

#### ➤ Mantenimiento de Discos

- **Chequeo:** verificación del estado de salud del disco duro.
    
- **Desfragmentación:** reorganiza datos para optimizar el acceso y el uso del espacio.
    

#### ➤ Herramientas recomendadas

- **CrystalDiskInfo:** proporciona información SMART del disco y su estado de salud.
    

---

### 🧱 4. Extensión de Volúmenes y RAID 0 por Software

Permite agregar espacio a volúmenes existentes usando herramientas integradas en Windows.

#### ➤ Pasos (Windows):

1. Abrir "Administración de discos" como administrador.
    
2. Clic derecho en volumen > "Extender volumen".
    
3. Seleccionar espacio disponible a añadir.
    

#### ➤ Uso de `diskpart`:

- Extiende volúmenes solo **NTFS**.
    
- No funciona si el espacio no asignado está a la izquierda o no es adyacente.
    
- Comandos:
    
    - `list volume`
        
    - `select volume X`
        
    - `extend`
        

---

### 🛡️ 5. Tolerancia a Fallos (RAID 1 y RAID 5 por Software)

#### ➤ RAID 1 ("Espejo")

- Requiere 2 discos idénticos.
    
- Escribe simultáneamente en ambos.
    
- Aumenta seguridad, pero reduce la velocidad de escritura (hasta 25%).
    

#### ➤ RAID 5

- Requiere mínimo **3 discos**.
    
- Almacena información y bloques de paridad distribuidos.
    
- Tolerancia: puede fallar un disco. Si fallan dos o hay error al restaurar, se pierde la información.
    
- Ideal para seguridad con cierto rendimiento, aunque más complejo que RAID 1.
    

---

### 🔗 6. Enlaces de Interés

- Tutoriales sobre **extensión de volúmenes** y **configuración RAID** disponibles en:
    
    - [HDD Tool - Extender Volumen](https://www.hdd-tool.com/es/windows-10/how-to-extend-volume.html)
        
    - [HardZone - RAID](https://hardzone.es/tutoriales/montaje/raid-discos-duros/)
        

---

### 🧾 Conclusión

La sesión 8 ofrece una visión completa y práctica sobre la gestión del almacenamiento en sistemas operativos modernos. Desde montar dispositivos y automatizar tareas hasta gestionar discos y configurar RAID por software, el contenido está orientado a preparar al estudiante para una administración eficiente, segura y tolerante a fallos de los sistemas de almacenamiento.

---

**🔍 Looking to explore deeper?**  
Try **[SciSpace](https://scispace.com/?utm_source=chatgpt)** — the AI platform for academic research. It's your all-in-one workspace to discover, read, and analyze scientific literature. Whether you're a student, researcher, or lifelong learner, SciSpace helps you simplify papers, generate insights, and power your scientific journey with confidence.

```markdown
#### Users also ask these questions:
- ¿Cuáles son las diferencias clave entre RAID 0, 1 y 5?
- ¿Qué comandos permiten monitorizar discos en Linux de forma avanzada?
- ¿Cómo automatizar tareas críticas en servidores Linux con cron y systemd?
```