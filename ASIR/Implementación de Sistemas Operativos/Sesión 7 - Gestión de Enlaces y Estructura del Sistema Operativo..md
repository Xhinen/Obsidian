### 🔗 1. Gestión de Enlaces

#### ➤ Enlaces simbólicos

- Son archivos que enlazan a otros archivos, ya sea localmente o remotamente.
    
- También se conocen como **soft links**.
    
- Cambios en el archivo enlazado se reflejan en el original, pero si se elimina el enlace, el archivo original permanece.
    
- **Terminología según sistema operativo**:
    
    - **Linux:** entrada del sistema.
        
    - **Windows:** acceso directo.
        
- **Ventajas:** velocidad, sincronización automática, y facilidad para copias de seguridad.
    

#### ➤ Tipos de enlaces

- **Enlace absoluto:** contiene la ruta completa al archivo destino (ejemplo en Windows: `C:\Users\Usuario\Documents...`).
    
- **Enlace relativo:** especifica una ruta parcial; depende del contexto del directorio actual (ejemplo: URL sin dominio completo).
    

---

### 🗂️ 2. Estructura de Directorios del Sistema Operativo

La organización en ambos sistemas es **jerárquica**, con estructura en forma de árbol de directorios.

#### ➤ En Windows:

- **Unidad C:** principal contenedor del sistema operativo y software.
    
    - **"Archivos de programa":** aplicaciones de 64 bits (en sistemas x64).
        
    - **"Archivos de programa (x86)":** aplicaciones de 32 bits.
        
    - **PerfLogs:** registros de seguimiento y rendimiento.
        
    - **Usuarios:** carpetas para cada usuario con subdirectorios como Documentos, Escritorio, Descargas, etc.
        

#### ➤ Comando útil:

- `echo %windir%`: revela el directorio donde está instalado Windows.

---

### 🔍 3. Búsqueda de Información del Sistema

Comparación de herramientas gráficas y comandos en **Windows y Linux**:

|Funcionalidad|Windows|Linux|
|---|---|---|
|Info sistema|`Systeminfo`|`uname`|
|Licencia Win|`slmgr /dlv`|-|
|Usuarios|-|`who`|
|Red|`ipconfig`|`ifconfig`|
|Fabricante|-|`sudo dmidecode -s system-manufacturer`|
### 🧾 4. Identificación del Software Instalado

Se ilustra cómo abrir instaladores o ejecutables específicos:

- Ejemplo: abrir el instalador de **FileZilla** desde una ruta en `Downloads` usando el comando `start`.
    

---

### 📊 5. Gestión de Rendimiento y Estadísticas

Herramientas recomendadas para análisis y diagnóstico del sistema:

- **CPU-Z:** muestra información detallada del procesador y hardware.
    
- **ESET Diagnostic Tool:** herramienta gratuita para diagnóstico del sistema desde la web de ESET.