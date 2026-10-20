#  API REST - Gestión de Usuarios

API RESTful desarrollada con **Django** y **Django REST Framework (DRF)** para la gestión y administración de usuarios, construida siguiendo una arquitectura en capas (DAO/DTO) e integrada con **PostgreSQL** mediante contenedores de **Docker**. Incluye documentación interactiva OpenAPI/Swagger.

---

##  Tecnologías Utilizadas

* **Lenguaje:** Python 3.x
* **Framework:** Django / Django REST Framework
* **Base de Datos:** PostgreSQL
* **Contenerización:** Docker & Docker Compose
* **Documentación:** Swagger UI / drf-yasg
* **Otras Librerías:** `python-decouple` (Manejo de `.env`), `dataclasses`

---

##  Arquitectura del Proyecto

El proyecto implementa un patrón en capas para desacoplar la lógica de negocio de la capa de persistencia:

```text
gestion_usuarios/
├── DAO/           # Data Access Objects (Consultas e interacción con PostgreSQL)
├── DTO/           # Data Transfer Objects (Estructuras de transferencia de datos)
├── exceptions/    # Excepciones personalizadas para manejo de errores HTTP
├── models.py      # Modelo de datos Usuario (UUID, campos auditables)
├── serializers.py # Serializadores de DRF
├── views.py       # ViewSets y controladores de endpoints
└── urls.py        # Enrutamiento local de la API
