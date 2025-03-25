# Auth Service

Este repositorio contiene el código del microservicio de **Autenticación y Gestión de Roles** del CRM modular. El microservicio se encarga de gestionar la autenticación segura mediante JWT (JSON Web Tokens), el control de acceso basado en roles (RBAC), y proporcionar seguridad centralizada para todos los módulos del sistema.

---

## Funcionalidades Clave

- **Autenticación de Usuarios:**
  - Validación de credenciales y generación de tokens JWT.
  - Expiración configurable de los tokens.

- **Control de Acceso (RBAC):**
  - Gestión de roles y permisos para restringir el acceso a recursos específicos.
  - Verificación de roles al consumir endpoints protegidos.

- **Gestión de Sesiones:**
  - Endpoint para consultar la información del usuario autenticado.
  - Opcional: invalidación de tokens mediante listas de revocación.

---

## Requisitos Previos

- **Python 3.9 o superior:** Asegúrate de tener Python instalado en tu sistema.
- **PostgreSQL:** Base de datos para almacenar usuarios, roles y permisos.
- **Docker:** Opcional, para ejecutar el servicio en un entorno contenedor.

---

## Estructura del Proyecto

El microservicio sigue la **arquitectura hexagonal**, separando la lógica de negocio de las dependencias externas.

auth-service/ 
├── app/ 
│ ├── dominio/ # Entidades: Usuarios, Roles, Permisos 
│ ├── aplicacion/ # Casos de uso: Autenticación, Gestión de Roles 
│ ├── infraestructura/ # Adaptadores: persistencia, validación de contraseñas 
│ └── interfaces/ # Endpoints REST y validaciones de datos 
├── tests/ # Pruebas unitarias y de integración 
├── Dockerfile # Configuración de contenedor 
├── requirements.txt # Dependencias del proyecto 
└── README.md # Documentación del servicio