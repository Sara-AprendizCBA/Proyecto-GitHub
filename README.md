

# 📚 Informe Detallado: Explorando Git y GitHub  
**Autora:** Sara Lucía Rodríguez Olmos  
**Programa:** Análisis y Desarrollo de Software (ADSO)  
**Ficha:** 3293689  
**Fecha:** 21 Octubre 2025  

---




## 📝 Introducción

En el entorno actual del **desarrollo de software**, caracterizado por su dinamismo, trabajo en equipo y constante evolución, **llevar un control preciso y estructurado de los cambios** realizados en los proyectos es una necesidad fundamental. A medida que los equipos crecen y los sistemas se vuelven más complejos, se hace imprescindible contar con herramientas que permitan **registrar versiones, revertir modificaciones, coordinar esfuerzos y garantizar la integridad del código fuente**.

Históricamente, los desarrolladores gestionaban versiones de sus programas de forma manual, guardando copias con nombres como “versión_final_ahora_sí_3”. Este método era ineficiente, propenso a errores y prácticamente inviable para proyectos colaborativos. Con el tiempo surgieron sistemas centralizados como CVS y Subversion (SVN), que permitieron llevar un control más estructurado, pero dependían de un único servidor central, lo que generaba limitaciones y vulnerabilidades.

En este contexto, en 2005 **Linus Torvalds**, creador del kernel de Linux, desarrolló **Git**, un sistema de control de versiones **distribuido**, rápido y seguro, pensado para coordinar a miles de desarrolladores trabajando en un mismo proyecto sin necesidad de depender de un único repositorio central. Git marcó un antes y un después, ofreciendo una arquitectura flexible, descentralizada y extremadamente eficiente para el versionamiento de código.

Paralelamente, surgió **GitHub**, una plataforma en la nube que aprovecha la potencia de Git y la combina con un entorno colaborativo moderno: permite alojar repositorios, gestionar equipos, revisar cambios mediante “pull requests”, reportar incidencias, documentar proyectos y automatizar flujos de trabajo. GitHub no solo es un repositorio de código: es una **red social para desarrolladores**, donde se construyen proyectos de manera abierta, transparente y organizada.

Este informe —elaborado en formato `README.md`— tiene como propósito **analizar, documentar y aplicar** los fundamentos de Git y GitHub a partir del estudio detallado de dos recursos audiovisuales fundamentales:

1. [Video 1: Git desde cero](https://youtu.be/jGehuhFhtnE)  
2. [Video 2: Aprende Git en 1 hora](https://youtu.be/VdGzPZ31ts8)  

A través de este análisis se busca:
- Comprender la lógica interna de Git como sistema de control de versiones.  
- Explorar la plataforma GitHub y sus funciones clave.  
- Aplicar comandos y flujos de trabajo reales en un repositorio práctico.  
- Reflexionar sobre la importancia del control de versiones en entornos académicos y profesionales.  

El documento combina un **enfoque técnico** (guías y comandos paso a paso) con un **enfoque académico** (análisis conceptual y crítico), con el objetivo de ofrecer una visión sólida y profunda que pueda servir tanto como guía práctica como sustento teórico para proyectos futuros.

---




## 🧠 1. Conceptos Fundamentales

### 🔸 ¿Qué es Git?

**Git** es un sistema de control de versiones distribuido que permite gestionar, registrar y organizar los cambios realizados en los archivos de un proyecto a lo largo del tiempo. Su característica más distintiva es que **cada desarrollador posee en su máquina una copia completa del repositorio**, incluyendo todo el historial y las versiones, lo que elimina la dependencia de un único servidor central y ofrece una gran flexibilidad para trabajar sin conexión.




#### 📜 Breve historia de Git

Antes de Git, el desarrollo del kernel de Linux utilizaba un sistema propietario llamado BitKeeper. Cuando su licencia cambió en 2005, Linus Torvalds decidió crear una herramienta propia con tres requisitos fundamentales:
1. **Velocidad extrema** para gestionar miles de commits de cientos de desarrolladores.  
2. **Diseño distribuido**, sin un único punto de fallo.  
3. **Integridad criptográfica** en cada cambio, garantizada mediante hashes SHA-1.

En menos de un mes, nació Git, que rápidamente fue adoptado por la comunidad y hoy en día es el estándar de facto en el desarrollo de software a nivel mundial.




#### 🧰 Características técnicas clave de Git

- **Versionamiento completo y local:** Cada usuario tiene todo el historial, lo que permite trabajar sin internet y realizar operaciones complejas rápidamente.  
- **Ramas ligeras y flexibles:** Git facilita la creación de ramas paralelas para experimentar sin afectar la línea principal de desarrollo.  
- **Comprobación de integridad:** Cada cambio es identificado mediante un hash SHA-1, lo que garantiza que ningún archivo o historial pueda alterarse sin ser detectado.  
- **Fusión eficiente:** Git integra cambios de diferentes ramas de manera inteligente, permitiendo colaboración masiva.  
- **Historial inmutable:** Una vez registrado, el historial de cambios forma una línea temporal clara y auditable.

Git no solo gestiona versiones: **modela la historia de un proyecto** de forma estructurada, lo que permite a los equipos tomar decisiones informadas, recuperar versiones anteriores y coordinar tareas con precisión.

---




### 🔸 ¿Qué es GitHub?

**GitHub** es una plataforma web lanzada en 2008 que permite alojar repositorios Git y extender sus funcionalidades a un entorno colaborativo global. Se ha convertido en el principal espacio donde desarrolladores, empresas y comunidades alojan y comparten su código.





#### 🌐 Principales funcionalidades de GitHub

- **Alojamiento de repositorios:** públicos (gratuitos) y privados.  
- **Control de acceso:** gestión de permisos para equipos y colaboradores.  
- **Pull Requests:** mecanismo para proponer y revisar cambios antes de fusionarlos.  
- **Issues y Projects:** herramientas para seguimiento de errores, tareas y planificación ágil.  
- **Wikis y documentación integrada:** ideal para proyectos educativos y profesionales.  
- **Acciones (GitHub Actions):** automatización de pruebas, despliegues y flujos CI/CD.

GitHub actúa como una **interfaz social y colaborativa** sobre Git. Proporciona un espacio donde los proyectos no solo se almacenan, sino que **viven y evolucionan** de manera abierta y participativa. Es ampliamente utilizado por organizaciones como Microsoft, Google y comunidades de software libre de todo el mundo.

---





## 🎥 2. Análisis de los Videos

### ▶️ **Video 1: Git desde cero** 

Este video introduce de forma clara y progresiva los fundamentos de Git. Comienza explicando qué es un sistema de control de versiones y por qué es útil, para luego pasar a la instalación y primeros pasos prácticos.

Posteriormente, se aborda la configuración global de identidad, necesaria para que Git registre correctamente los cambios asociados a cada usuario. Para ello se utilizan los siguientes comandos:

```bash
git config --global user.name "Nombre del Usuario"
git config --global user.email "correo@ejemplo.com"
```

Esto permite que cada commit (o confirmación de cambios) quede firmado con la identidad del desarrollador, garantizando trazabilidad.

Además, el video explica conceptos clave como “repositorio”, “working directory”, “staging area” y “commit history”.

-**El working directory es el espacio local donde se hacen cambios reales en los archivos.
-**La staging area funciona como una zona intermedia donde se preparan los cambios antes de confirmarlos.
-**Un commit es un “punto de control” que guarda el estado del proyecto en un momento dado, junto con un mensaje descriptivo.

También se enseña cómo inicializar un repositorio con:

```bash
git init
```

Y cómo llevar archivos a la zona de preparación y luego confirmar los cambios:

```bash
git add .
git commit -m "Primer commit"
```

Otro aspecto importante es la explicación de los hashes SHA-1, que Git genera para identificar de manera única cada commit. Esto proporciona seguridad, ya que cualquier alteración en el contenido cambia el hash, permitiendo detectar modificaciones no autorizadas.

El video concluye destacando cómo Git, al ser un sistema distribuido, permite trabajar sin conexión y revertir cambios fácilmente, lo que lo convierte en una herramienta poderosa para el desarrollo profesional.

👉 Este recurso se enfoca principalmente en la base técnica local de Git, es decir, todo lo que ocurre en la computadora del desarrollador antes de sincronizar con plataformas externas como GitHub.





### ▶️ **Video 2: Aprende Git en 1 hora** 

Este segundo video funciona como un curso intensivo y práctico que va más allá de la configuración básica, mostrando un flujo de trabajo completo que integra Git con GitHub. La explicación está organizada en módulos claros: creación de repositorios, conexión remota, ramas, colaboración y resolución de conflictos.

Primero, se muestra cómo crear un repositorio remoto en GitHub, y luego conectarlo con el repositorio local mediante:

```bash
git remote add origin https://github.com/usuario/repositorio.git
git branch -M main
git push -u origin main
```

Esta parte es fundamental porque establece el “puente” entre el trabajo local y la nube, permitiendo subir y compartir el código con otros desarrolladores.

A continuación, el video introduce el concepto de ramas (branches), explicando que estas permiten trabajar en nuevas funcionalidades sin alterar la versión principal del proyecto. Se muestran comandos como:

```bash
git branch nueva-rama
git checkout nueva-rama
```

o en versiones más recientes:

```bash
git switch -c nueva-rama
```

También se explica cómo fusionar ramas mediante git merge y cómo manejar posibles conflictos cuando dos personas modifican el mismo archivo. Se destacan las buenas prácticas, como hacer commits frecuentes, usar mensajes claros y mantener la rama principal (main o master) estable.

Una parte muy valiosa del video es la colaboración mediante “pull requests”, donde se simula el flujo de trabajo profesional: un desarrollador hace cambios en una rama, los sube a GitHub y luego abre un Pull Request para que otro miembro del equipo revise y apruebe los cambios antes de fusionarlos. Esta práctica mejora la calidad del código y promueve la revisión colectiva.

Además, se abordan temas como:

- **Clonación de repositorios existentes (git clone).
- **Sincronización de cambios remotos (git pull).
- **Actualización de cambios locales en GitHub (git push).
- **Configuración de llaves SSH para conexiones seguras.
- **Creación de archivos .gitignore para excluir archivos innecesarios del control de versiones.

El video combina teoría y práctica de manera efectiva, mostrando ejemplos reales que reflejan cómo se trabaja en proyectos colaborativos profesionales. También enfatiza la importancia de mantener una estructura clara, usar ramas temáticas y seguir convenciones para mensajes de commit.

👉 En conclusión, este video permite entender el flujo completo de trabajo con Git y GitHub, desde la creación local hasta la 
colaboración remota, cubriendo tanto las herramientas como las buenas prácticas de trabajo en equipo.





### ▶️ **Conclusión del análisis** 

Ambos videos se complementan perfectamente:

El primero construye una base sólida sobre el funcionamiento interno de Git, centrándose en el trabajo local, la estructura de un repositorio y los comandos fundamentales.

El segundo amplía ese conocimiento para mostrar cómo integrar Git con GitHub y trabajar de manera colaborativa en proyectos reales, incluyendo ramas, sincronización remota y revisión de código. 

En conjunto, estos recursos ofrecen una formación integral que va desde la teoría inicial hasta la práctica profesional. Gracias a ellos, se puede comprender no solo qué comandos usar, sino por qué y cuándo utilizarlos, lo que fortalece las competencias técnicas en control de versiones y trabajo colaborativo en desarrollo de software.
