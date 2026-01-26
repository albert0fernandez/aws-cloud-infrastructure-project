# 🎨 Academia de Pintura: Solución Cloud de Alta Disponibilidad

[![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://www.php.net/)

Este proyecto consiste en el diseño e implementación de una infraestructura en la nube para una academia de pintura, priorizando la **alta disponibilidad (24/7)**, la **seguridad** y la **optimización de costes**. Desarrollado como parte del reto **RetaCantabria 2025/2026**.

---

## 🏗️ Arquitectura del Sistema
La solución se apoya íntegramente en los servicios de **Amazon Web Services (AWS)** para garantizar un entorno escalable y seguro.




| Servicio AWS | Categoría | Función en el Proyecto |
| :--- | :--- | :--- |
| **VPC** | Networking | Segmentación de red con subredes públicas y privadas. |
| **EC2** | Computación | Hosting de la aplicación PHP y WordPress (Glosario). |
| **ALB & ASG** | Escalabilidad | Balanceador de carga y auto-escalado para alta disponibilidad. |
| **RDS (MySQL)** | Base de Datos | Base de Datos relacional gestionada para la app principal. |
| **S3** | Almacenamiento | Destino de backups diarios automatizados vía cron. |
| **Lambda** | Automatización | Ejecución de código sin servidores para tareas programadas. |
| **CloudFormation** | IaC | Despliegue automático de recursos mediante plantillas YAML. |
| **SNS** | Mensajería | Servicio sencillo de notificaciones y alertas. |
| **CloudWatch** | Monitorización | Monitorización y observabilidad de todo el sistema cloud. |

---

   graph LR
    subgraph "Capa de Computación (EC2)"
        A[Script de Backup / Cron Job] -- "1. Genera .sql y sube" --> B
    end

    subgraph "Capa de Almacenamiento y Eventos (AWS)"
        B[(Amazon S3 Bucket)] -- "2. Evento: ObjectCreated" --> C(AWS Lambda)
        C -- "3. Procesa y Valida" --> D[Amazon SNS]
    end

    subgraph "Notificaciones"
        D -- "4. Alerta de Éxito/Error" --> E{Administrador}
    end

    style B fill:#f96,stroke:#333,stroke-width:2px
    style C fill:#69f,stroke:#333,stroke-width:2px
    style D fill:#f66,stroke:#333,stroke-width:2px


## 🔐 Seguridad y Administración
Como administrador del sistema, implementé las siguientes mejoras de seguridad y eficiencia:
- **Backup Automation:** Implementación de `cron jobs` para copias de seguridad diarias en **S3**.
- **Acceso Seguro:** Gestión de accesos mediante claves SSH personalizadas y despliegue de firewall mediante Grupos de Seguridad.
- **Base de Datos Robusta:** Uso de **Triggers** para el archivado automático de registros (`_archivadas`), garantizando la integridad de los datos históricos.

---

## 💰 Optimización de Costes
Uno de los pilares del proyecto fue minimizar el gasto operativo. 
- Se realizó un análisis detallado del nivel gratuito de AWS.
- Se configuraron políticas de apagado y dimensionamiento adecuado (Right-sizing) de instancias.
- [Consulta el análisis de costes detallado aquí](./docs/analisis_costes.pdf).

---

## 🛠️ Tecnologías
- **Backend:** PHP, Python (Lambda).
- **Frontend:** HTML, CSS, JavaScript (Paginación y ordenación).
- **CMS:** WordPress (Glosario técnico).
- **Herramientas:** Git, CloudFormation.

---



---
*Este proyecto es una demostración de competencias en administración de sistemas y arquitectura cloud.*
