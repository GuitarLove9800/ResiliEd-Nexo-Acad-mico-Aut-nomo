# Proyecto ResiliEd: Nexo Académico Autónomo
**Subtítulo:** Plataforma de Contingencia y Continuidad Académica Local  
**Institución:** Tecnológico de Software  
**Equipo:** Equipo 3  
**Integrantes:**
- Daniel Romero
- Aaron Diaz
- Emmanuel Alexander Poot Vazquez

---

## 1. Definición clara del problema

En el entorno académico actual, la dependencia total hacia plataformas propietarias centralizadas en la nube (tales como Microsoft Teams o Google Classroom) genera una vulnerabilidad crítica en la continuidad escolar. Cuando estos servicios sufren caídas de infraestructura global, fallas en sus servidores de autenticación (por ejemplo, Azure AD) o suspensiones por mantenimiento, el flujo de trabajo académico se interrumpe de forma abrupta e inmediata.

Esta desconexión deja a estudiantes y docentes sin canales alternativos para recibir avisos urgentes, consultar fechas límite o enviar tareas críticas, resultando en desorganización y retrasos no atribuibles al alumnado.

---

## 2. Objetivo general y propuesta de solución

* **Objetivo General:** Desarrollar una plataforma web de contingencia ligera, autónoma y de despliegue local o independiente, que asegure la comunicación esencial y la entrega oportuna de actividades académicas ante caídas o indisponibilidad de las plataformas centrales.
* **Propuesta de Solución:** Crear un entorno web centralizado para la institución que opere de manera paralela y ligera. El sistema dispondrá de un tablero de anuncios prioritarios emitidos por docentes y un módulo directo de recepción de tareas con comprobante digital, permitiendo mantener la actividad formativa sin depender de la infraestructura de terceros.

##
---

## 3. Definición del alcance

### Elementos incluidos (Dentro del alcance)

* **Entorno de ejecución local / red escolar:**
  * Despliegue del prototipo en entorno de desarrollo local (`localhost`) o red de área local (LAN) empleando un servidor local básico (Apache / Node.js) sin incurrir en costos de hosting o licencias.
* **Control de acceso y autenticación básica:**
  * Formulario de inicio de sesión (*login*) con validación de credenciales en base de datos relacional (MySQL).
  * Distinción funcional entre dos roles esenciales: **Profesor** y **Estudiante**.
* **Módulo de anuncios y avisos prioritarios:**
  * Panel docente para la publicación de avisos de contingencia (título, descripción, fecha de emisión).
  * Panel estudiantil para la visualización en orden cronológico de dichos comunicados.
* **Módulo esencial de entrega de tareas:**
  * Publicación de asignaciones por parte del docente con fecha y hora límite.
  * Formulario web para la carga y almacenamiento de archivos ligeros (formatos estándar como `.pdf` o `.zip`) con registro de marca de tiempo (*timestamp*) en base de datos.
* **Interfaz web responsiva:**
  * Diseño maquetado con HTML5 semántico y CSS3 adaptable para visualización correcta en computadoras de escritorio y navegadores móviles.

---

### Elementos no incluidos (Fuera del alcance)

Las siguientes funcionalidades quedan excluidas debido a limitaciones técnicas, de tiempo, infraestructura y presupuesto. A continuación se desglosan los requerimientos necesarios para una hipotética fase de escalabilidad institucional:

#### 1. Infraestructura física y servidores propios dedicados
* **¿Por qué queda fuera?:** El equipo no cuenta con presupuesto ni instalaciones de telecomunicaciones para hospedar un servidor físico institucional.
* **¿Qué se requeriría?:**
  * *Hardware físico:* Al menos un servidor para rack o torre empresarial (procesador multinúcleo tipo Intel Xeon / AMD EPYC, mínimo 32-64 GB de memoria RAM ECC y almacenamiento en arreglo RAID SSD/NVMe redundante).
  * *Infraestructura de soporte:* Sistema de alimentación ininterrumpida (UPS / No-Break empresarial), sistema de ventilación/climatización para centro de datos y una conexión simétrica de fibra óptica con IP pública estática y enlace de respaldo.
* **Estimación de inversión:** Alrededor de $\$35,000 - \$60,000$ MXN en equipamiento inicial básico, sin contemplar costos mensuales recurrentes de energía eléctrica y ancho de banda dedicado.

#### 2. Streaming de video y conferencias en tiempo real
* **¿Por qué queda fuera?:** Transmitir video en vivo para múltiples grupos simultáneos saturaría cualquier servidor casero o de pruebas y requiere una arquitectura de red compleja.
* **¿Qué se requeriría?:**
  * *Software / Protocolos:* Servidores de medios especializados basados en WebRTC (ej. Jitsi Core, mediasoup o Kurento), balanceadores de carga (*load balancers*) y códecs de compresión adaptativa.
  * *Conocimientos técnicos:* Gestión avanzada de sockets, protocolos de transporte UDP/RTP, optimización de latencia de red y manejo de concurrencia a nivel de sistemas operativos.
* **Estimación de inversión:** Servidores en la nube con alto ancho de banda o clusters dedicados (estimado de $\$2,500 - \$7,000$ MXN mensuales en servicios de nube tipo AWS EC2 / DigitalOcean según el volumen de alumnos).

#### 3. Chat instantáneo y mensajería síncrona
* **¿Por qué queda fuera?:** Implementar mensajería en tiempo real requiere tecnologías que aún no se abordan en el mapa curricular de primer cuatrimestre y elevaría el riesgo de no concluir a tiempo el proyecto base.
* **¿Qué se requeriría?:**
  * *Software / Librerías:* Servidores WebSocket persistentes (Node.js con Socket.io), bases de datos en memoria para almacenamiento en caché rápida (Redis).
  * *Conocimientos técnicos:* Programación asíncrona reactiva, eventos en tiempo real, control de estado de conexiones socket y prevención de saturación por peticiones concurrentes.

#### 4. Alta disponibilidad y seguridad institucional de nivel productivo
* **¿Por qué queda fuera?:** Excede el tiempo límite de cuatro semanas; el proyecto se enfocará en hashing de contraseñas y validación básica de entradas.
* **¿Qué se requeriría?:**
  * *Software y Seguridad:* Certificados SSL/TLS dedicados, cortafuegos de aplicaciones web (WAF como Cloudflare Enterprise o ModSecurity), protección anti-DDoS, políticas de respaldo automatizado en ubicaciones externas y cumplimiento de leyes de privacidad de datos personales.
  * *Conocimientos técnicos:* Ciberseguridad ofensiva y defensiva, hardening de servidores Linux, auditorías de vulnerabilidades (inyecciones SQL avanzadas, XSS, CSRF) y administración de bases de datos a escala empresarial (DBA).
* **Estimación de inversión:** Certificaciones, dominios, licencias de monitoreo y soporte especializado estimado entre $\$8,000 - \$15,000$ MXN anuales.



##

### Apartir de aqui va la parte de Daniel(despues de agregar tu parte, borra esta linea)

