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

bash
npm install
npm start


## 5.1.2 Source Code Management

El proyecto se gestionó utilizando GitHub, lo cual permitió llevar un control claro de todos los cambios realizados durante el desarrollo de MineTrack.

Se utilizó una estructura de ramas sencilla pero efectiva, que facilitó el trabajo en equipo y evitó conflictos:

- **main:** versión estable del proyecto  
- **develop:** integración de nuevas funcionalidades  
- **feature/\*:** desarrollo de nuevas características  
- **fix/\*:** corrección de errores  

El flujo de trabajo consistía en crear una rama a partir de `develop`, implementar la funcionalidad asignada, realizar commits con mensajes claros y finalmente crear un Pull Request para su revisión antes de integrarlo nuevamente.

Ejemplo de commit utilizado:

bash
git commit -m "feat: agregar monitoreo de maquinaria con datos IoT"

## 5.1.3 Source Code Style Guide & Conventions

Para mantener el código limpio y fácil de entender, se definieron algunas convenciones básicas que todos los integrantes del equipo siguieron durante el desarrollo.

Entre las principales reglas adoptadas se encuentran:

- Uso de camelCase para variables y funciones  
- Uso de PascalCase para clases y componentes  
- Indentación de 2 espacios  
- Organización del código en módulos reutilizables  
- Inclusión de comentarios en partes importantes del código  

Ejemplo:

javascript
function evaluarEstadoMaquina(sensor) {
  if (sensor.temperatura > 80) {
    return "Alerta";
  }
  return "Normal";
}
