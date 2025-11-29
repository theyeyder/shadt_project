Descripción General

El sistema SHADT es un prototipo funcional basado en las maquetas y definiciones realizadas en la Actividad 2. Su objetivo es simular la operación de un sistema hospitalario que permite administrar pacientes, registrar su evolución clínica y gestionar procesos como admisiones, signos vitales, historial, hospitalización, salida, informes y usuarios.

El proyecto fue desarrollado totalmente en HTML, CSS, JavaScript y LocalStorage, permitiendo funcionar sin backend.



* Características principales

Simulación de sistema hospitalario.

Módulos totalmente funcionales.

Persistencia local con localStorage.

Flujo completo de atención:
Admisión → Signos Vitales → Historia Clínica → Salida / Hospitalización.

Asignación de camas y monitoreo por estado.

Generación de informes.

Configuración y gestión de usuarios.

Interfaz modular, intuitiva y responsiva.

* Tecnologías utilizadas

HTML5

CSS3 / Bootstrap 5

JavaScript

LocalStorage

CSV export (simulado)


📁 Estructura del proyecto
/ (raíz del proyecto)
│── index.html
│── modulos.html
│── admision.html
│── signos_vitales.html
│── historia_clinica.html
│── salida.html
│── acostar.html
│── estadia_alta.html
│── informes.html
│── configuracion.html
│── css/
│── js/
│── img/
└── README.md

* Flujo general del sistema

Inicio de sesión

Selección del módulo

Registro de paciente y admisión

Registro de signos vitales

Creación de historia clínica

Decisiones:

Alta

Hospitalización

Asignación de cama

Estadía → Alta

Generación de informes

Administración de usuarios

* Descripción de cada módulo
 1. Pantalla de Login (index.html)

Campos:

Conexión

Usuario

Contraseña

Lógica:

Usuarios tipo Salud usan credenciales configuradas en el módulo de Configuración.

Usuarios especiales:

Admin

Desarrollador

Prueba

Soporte
→ Usuario y contraseña = conexión (Ej: usuario: admin / contraseña: admin)

Al ingresar:

Guarda usuario actual en localStorage.

Redirige a modulos.html.

2. Pantalla de Módulos (modulos.html)

Tarjetas de acceso rápido a cada sección.

En la esquina inferior izquierda muestra:

Usuario logueado en sesión.

 3. Módulo de Admisión (admision.html)

Permite:

Buscar paciente por tipo y número de documento.

Registrar/actualizar datos:

Datos personales

EPS

Ciudad

Dirección

Síntomas

Sexo

Acompañante

Estado del paciente

Control de admisiones:

Activa

Anulada

Revertida

 4. Módulo de Signos Vitales (signos_vitales.html)

Carga al paciente con admisión activa.

Permite registrar:

Frecuencia cardíaca

Temperatura

Cada registro se guarda en shadt_signos.

5. Módulo de Historia Clínica (historia_clinica.html)

Carga:

Datos base del paciente

Admisión activa

Permite guardar:

Diagnóstico

Enfermedad actual

Exámenes

Peso

Talla

Color de piel

Fórmula

Tratamiento

Estados: abierta / cerrada.

6. Módulo de Salida (salida.html)

Permite:

Dar salida (cierra la historia clínica)

Hospitalizar

Deja la historia abierta

Registra la decisión para los módulos posteriores

 7. Módulo Acostar Paciente (acostar.html)

Funcionalidades:

Asignación de camas.

Validaciones:

No duplicar cama

No acostar un paciente dos veces

Guarda:

Tipo de cama

Tipo de paciente (niño, adulto, embarazada)

 8. Módulo de Estadía y Alta (estadia_alta.html)

Mapa visual de camas con iconos según tipo de paciente.

Permite:

Seleccionar cama

Dar alta y liberar cama

 9. Módulo de Informes (informes.html)

Genera informes de:

Pacientes admisionados

Pacientes hospitalizados

Pacientes dados de altabb

Historias clínicas

Signos vitales

Incluye:

Filtro por rango de fechas

Vista en pantalla

Exportar CSV/Excel

Imprimir

 10. Módulo de Configuración de Usuarios (configuracion.html)

Permite:

Crear usuarios

Editar usuarios

Eliminar usuarios

Campos:

Nombre mostrado

Usuario (login)

Contraseña / Confirmación

Conexión:

Salud

Prueba

Soporte

Admin

Desarrollador

Estado: activo / inactivo

Además:

Permite seleccionar qué usuario queda como usuario actual.

⚙️ Funcionalidades adicionales

Persistencia total con LocalStorage.

Limpieza de datos por módulo.

Generación de identificadores únicos.

Control de estados para cada componente del sistema.

Iconografía para mejorar comprensión.

Sistema sin backend → ideal para prototipado rápido.

