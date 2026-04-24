### 4.6.1 Design-Level EventStorming

Se realizó una sesión de Design-Level EventStorming para identificar los principales eventos, actores y reglas de negocio del sistema MineTrack, considerando la interacción entre usuarios y sensores IoT.

#### Evidencia del Event Storming

![EventStorming](Resources/eventstorming-mineTrack.png)

### 4.6.2 Software Architecture Context Diagram

En esta sección se presenta el diagrama de contexto del sistema MineTrack, el cual ilustra la interacción del sistema con actores y sistemas externos. El sistema se representa en el centro, rodeado por los usuarios y servicios con los que interactúa.

MineTrack interactúa con tres actores principales:

User (Usuario): Son los usuarios finales que monitorean el estado de la maquinaria, visualizan información y reciben alertas y reportes.

Maintenance Company (Empresa de Mantenimiento): Encargada de programar y gestionar el mantenimiento, revisar historiales y monitorear las condiciones de la maquinaria.

Administrator (Administrador): Responsable de gestionar la configuración del sistema, usuarios y permisos de la plataforma.

Además, MineTrack interactúa con sistemas externos:

IoT Sensors (Sensores IoT): Proveen datos en tiempo real como temperatura, vibración y horas de uso de la maquinaria.

Database System (Sistema de Base de Datos): Almacena la información del sistema, datos de maquinaria y registros de usuarios.

Notification Service (Servicio de Notificaciones): Envía alertas y notificaciones a los usuarios mediante diferentes canales.

El diagrama muestra cómo MineTrack integra estos componentes para ofrecer una solución completa de monitoreo y gestión de maquinaria.
![Context Diagram](Resources/context-diagram.png)
