# Inventario Service

Este repositorio contiene el código del microservicio de **Gestión de Inventarios** del CRM modular. El microservicio permite la actualización en tiempo real de existencias, generación de alertas (stock bajo, caducidad próxima), optimización predictiva mediante Machine Learning y la coordinación con proveedores para garantizar una gestión eficiente del inventario.

---

## Funcionalidades Clave

- **Gestión en Tiempo Real:**
  - Actualización automática del inventario mediante sensores IoT (RFID, códigos QR).
  - Entrada manual de datos para ajustes operativos.
  - Alertas automáticas para stock bajo, productos obsoletos o próximos a caducar.

- **Optimización Predictiva:**
  - Modelos de Machine Learning para predecir demanda y sugerir reabastecimiento.
  - Dashboards interactivos con métricas clave como rotación de inventario, costos y clasificación de productos.

- **Coordinación con Proveedores:**
  - Generación automática de órdenes de compra al alcanzar niveles mínimos de inventario.
  - Sincronización con sistemas externos para evitar sobrestock y garantizar reabastecimiento a tiempo.

---

## Requisitos Previos

- **Python 3.9 o superior:** Asegúrate de tener Python instalado en tu sistema.
- **PostgreSQL:** Base de datos para transacciones principales.
- **MongoDB:** Para almacenar datos no estructurados, como historial de inventarios y logs.
- **Docker:** Opcional, para ejecutar el servicio en un entorno contenedor.

---

## Estructura del Proyecto

El microservicio sigue la **arquitectura hexagonal**, separando la lógica de negocio de las dependencias externas.

inventario-service/
├── app/
│ ├── dominio/ # Entidades, reglas y modelos del negocio 
│ ├── aplicacion/ # Casos de uso y servicios 
│ ├── infraestructura/ # Adaptadores: persistencia, APIs externas 
│ └── interfaces/ # Endpoints REST y validaciones de datos 
├── tests/ # Pruebas unitarias y de integración 
├── Dockerfile # Configuración de contenedor 
├── requirements.txt # Dependencias del proyecto 
└── README.md #