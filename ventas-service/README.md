# Ventas Service

Este repositorio contiene el código del microservicio de **Gestión de Ventas** del CRM modular. El microservicio se encarga de manejar el pipeline de ventas, el seguimiento de leads, la automatización de tareas, y la integración con herramientas externas para maximizar la eficiencia del equipo comercial.

---

## Funcionalidades Clave

- **Pipeline de Ventas Inteligente:**
  - Gestión de etapas: Prospección, Calificación, Propuesta, Negociación, Cierre.
  - Automatización de tareas repetitivas (recordatorios, envíos de propuestas).

- **Seguimiento de Leads y Oportunidades:**
  - Historial completo de interacciones.
  - Sistema de scoring para priorización de leads según criterios configurables.

- **Integración con Herramientas Externas:**
  - Sincronización bidireccional con LinkedIn Sales Navigator, Gmail/Outlook y calendarios.
  - Envío de mensajes personalizados a redes sociales o por correo desde el CRM.

---

## Requisitos Previos

- **Python 3.9 o superior:** Asegúrate de tener Python instalado en tu sistema.
- **PostgreSQL:** Base de datos transaccional para la persistencia de datos.
- **MongoDB (opcional):** Para almacenar datos no estructurados.
- **Docker (opcional):** Para ejecutar el servicio en un entorno contenedor.

---

## Estructura del Proyecto

El microservicio sigue la **arquitectura hexagonal** para separar la lógica de negocio de las dependencias externas.

ventas-service/ 
├── app/
│ ├── dominio/ # Lógica del negocio: Entidades, Reglas 
│ ├── aplicacion/ # Casos de uso y servicios de aplicación
│ ├── infraestructura/ # Adaptadores: persistencia, APIs externas
│ └── interfaces/ # Endpoints REST, validaciones
├── tests/ # Pruebas unitarias e integrales
├── Dockerfile # Configuración para contenedores
├── requirements.txt # Dependencias del proyecto
└── README.md