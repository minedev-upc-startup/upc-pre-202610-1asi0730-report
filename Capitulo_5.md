# Capítulo V: Product Implementation, Validation & Deployment

## 5.1 Software Configuration Management

Para el desarrollo de MineTrack se siguió un enfoque ordenado en la gestión de configuración del software. Esto permitió que todos los integrantes trabajen sobre una misma base, evitando errores y manteniendo coherencia en cada cambio realizado.

MineTrack es una solución enfocada en mejorar el proceso de venta y mantenimiento preventivo de maquinaria, apoyándose en dispositivos IoT que permiten obtener datos en tiempo real. Por ello, era importante asegurar que tanto el código como las configuraciones se mantengan controladas durante todo el desarrollo.

---

## 5.1.1 Software Development Environment Configuration

Desde el inicio del proyecto, se definió un entorno de desarrollo común para todo el equipo. Esto ayudó a evitar problemas de compatibilidad y facilitó la integración del trabajo de cada integrante.

Las herramientas principales utilizadas fueron:

- **Frontend:** Angular  
- **Backend:** Node.js  
- **Lenguaje:** JavaScript / TypeScript  
- **Gestor de paquetes:** npm  
- **Editor recomendado:** Visual Studio Code  
- **Control de versiones:** Git  

Para ejecutar el proyecto, se siguieron pasos simples:

```bash
npm install
npm start
```

## 5.1.2 Source Code Management

El proyecto se gestionó utilizando GitHub, lo cual permitió llevar un control claro de todos los cambios realizados durante el desarrollo de MineTrack.

Se utilizó una estructura de ramas sencilla pero efectiva, que facilitó el trabajo en equipo y evitó conflictos:

- **main:** versión estable del proyecto  
- **develop:** integración de nuevas funcionalidades  
- **feature/\*:** desarrollo de nuevas características  
- **fix/\*:** corrección de errores  

El flujo de trabajo consistía en crear una rama a partir de `develop`, implementar la funcionalidad asignada, realizar commits con mensajes claros y finalmente crear un Pull Request para su revisión antes de integrarlo nuevamente.

Ejemplo de commit utilizado:

```bash
git commit -m "feat: agregar monitoreo de maquinaria con datos IoT"
```
## 5.1.3 Source Code Style Guide & Conventions

Para mantener el código limpio y fácil de entender, se definieron algunas convenciones básicas que todos los integrantes del equipo siguieron durante el desarrollo.

Entre las principales reglas adoptadas se encuentran:

- Uso de camelCase para variables y funciones  
- Uso de PascalCase para clases y componentes  
- Indentación de 2 espacios  
- Organización del código en módulos reutilizables  
- Inclusión de comentarios en partes importantes del código  

Ejemplo:

```javascript
function evaluarEstadoMaquina(sensor) {
  if (sensor.temperatura > 80) {
    return "Alerta";
  }
  return "Normal";
}
```

## 5.1.4 Software Deployment Configuration

El despliegue del sistema MineTrack se realizó considerando la necesidad de contar con una versión accesible del producto que permita mostrar su funcionamiento de manera clara.

Para ello, se generó una versión de producción del proyecto utilizando el siguiente comando:

```bash
npm run build
```
Este proceso permitió optimizar la aplicación para su ejecución en un entorno real, reduciendo el tamaño de los archivos y mejorando el rendimiento.

Posteriormente, la aplicación fue desplegada en un entorno web, lo que permitió validar que el sistema funcione correctamente fuera del entorno de desarrollo.

De esta manera, se logró contar con una Landing Page funcional que presenta la propuesta de valor del sistema MineTrack, enfocada en la venta y mantenimiento preventivo inteligente de maquinaria mediante el uso de dispositivos IoT.

## 5.2 Landing Page, Services & Applications Implementation
### 5.2.1 Sprint 1
## 5.2.1 Sprint 1

En esta sección se describe el desarrollo del Sprint 1 del proyecto MineTrack, incluyendo la planificación, organización del equipo, backlog del sprint y evidencias de implementación.

El Sprint 1 se enfocó en la construcción inicial del Landing Page, así como la configuración del entorno de desarrollo y la estructura base del proyecto, permitiendo al equipo establecer una base sólida para los siguientes sprints.

Durante este Sprint, el equipo trabajó de manera colaborativa, distribuyendo responsabilidades y estableciendo objetivos claros, alineados con el cumplimiento del Student Outcome 5, el cual enfatiza la planificación efectiva, liderazgo compartido y trabajo en equipo.

### 5.2.1.1 Sprint Planning 1

En esta sección se describen los aspectos principales del Sprint Planning Meeting correspondiente al Sprint 1, donde el equipo definió los objetivos, alcance y organización del trabajo.

| Sprint # | Sprint 1 |
|----------|---------|
| **Sprint Planning Background** |  |
| Date | 2026-04-20 |
| Time | 08:00 PM |
| Location | Reunión virtual vía Discord|
| Prepared By | Meza Huanacuna, Juan José |
| Attendees (to planning meeting) | Sanchez Arenas, Zahir Emmanuel / Mendoza Machoa, Lionel / Meza Huanacuna, Juan José / Aliquipa Poma, Sebastian Andres / Figueroa Sanchez, Alvaro / Molina Umeres, Nestor |
| Sprint 0 – Review Summary | No aplica, debido a que este es el primer Sprint del proyecto. |
| Sprint 0 – Retrospective Summary | No aplica, al ser el primer Sprint. |
| **Sprint Goal & User Stories** | |
| Sprint 1 Goal | **Our focus is on** developing the initial version of the Landing Page and setting up the development environment. <br> **We believe it delivers** a clear presentation of the value proposition to potential users and a solid base for future development. <br> **This will be confirmed when** the Landing Page is accessible and includes key sections such as Home, Features, and Contact.|
| Sprint 1 Velocity | El equipo definió una capacidad de trabajo de **15 Story Points** para este Sprint, considerando la disponibilidad de los integrantes. | 
| Sum of Story Points| La suma total de Story Points asignados a las User Stories seleccionadas para este Sprint es de: **15 Story Points**  |


### 5.2.1.2 Aspect Leaders and Collaborators

En esta sección se presenta la matriz de liderazgo y colaboración (LACX), la cual define, para cada aspecto del Sprint 1, quién asume el rol de líder (Leader) y quiénes participan como colaboradores (Collaborators).

Los aspectos seleccionados están directamente relacionados con el alcance del Sprint 1, el cual se centró en la implementación inicial del Landing Page y la configuración del entorno de desarrollo del sistema MineTrack.

Los principales aspectos considerados fueron:

- Desarrollo del Landing Page  
- Configuración del entorno de desarrollo  
- Gestión del repositorio en GitHub  
- Diseño de interfaz (UI/UX)  
- Documentación del proyecto  

Esta distribución permite mejorar la organización del equipo, asignando responsabilidades claras y fomentando la colaboración activa, en línea con el cumplimiento del Student Outcome 5.

---

### Leadership and Collaboration Matrix (LACX)

| Team Member (Last Name, First Name) | GitHub Username | Landing Page | Entorno Dev | GitHub | UI/UX | Documentación |
|------------------------------------|----------------|--------------|-------------|--------|-------|--------------|
| Sanchez Arenas, Zahir Emmanuel | zahirsanchez | L | C | C | L | C |
| Mendoza Machoa, Lionel | lionelmendoza | C | L | C | C | L |
| Meza Huanacuna, Juan José | JuanMHZ12 | L | C | L | C | C |
| Aliquipa Poma, Sebastian Andres | sebastianaliquipa | C | C | C | L | C |
| Figueroa Sanchez, Alvaro | alvarofigueroa | C | L | C | C | L |
| Molina Umeres, Nestor | nestormolina | C | C | L | C | C |

---

### Leyenda

- **L (Leader):** Responsable principal del aspecto  
- **C (Collaborator):** Apoyo en la ejecución del aspecto  

---

### Justificación

La asignación de líderes y colaboradores se realizó considerando la distribución equitativa de responsabilidades y la participación activa de todos los integrantes del equipo.

Cada miembro asumió al menos un rol de liderazgo, lo cual permitió fortalecer la coordinación interna y asegurar el cumplimiento de los objetivos del Sprint.

Además, esta organización está alineada con las tareas definidas en el Sprint Backlog, garantizando coherencia entre la planificación y la ejecución del trabajo.
### 5.2.1.3 Sprint Backlog 1
### 5.2.1.4 Development Evidence for Sprint Review
### 5.2.1.5 Execution Evidence for Sprint Review
### 5.2.1.6 Services Documentation Evidence for Sprint Review
### 5.2.1.7 Software Deployment Evidence for Sprint Review
### 5.2.1.8 Team Collaboration Insights during Sprint
