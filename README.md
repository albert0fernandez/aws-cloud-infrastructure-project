# 🎨 Academia de Pintura: Solución Cloud de Alta Disponibilidad

[![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://www.php.net/)

Este proyecto consiste en el diseño e implementación de una infraestructura en la nube para una academia de pintura, priorizando la **alta disponibilidad (24/7)**, la **seguridad** y la **optimización de costes**. Desarrollado como parte del reto **RetaCantabria 2025/2026**.

---

## 🏗️ Arquitectura del Sistema
La solución se apoya íntegramente en los servicios de **Amazon Web Services (AWS)** para garantizar un entorno escalable y seguro.



### Servicios Utilizados:
* **Computación & Escalabilidad:** EC2 con **Auto Scaling Group** y **Application Load Balancer (ALB)** para gestionar picos de tráfico.
* **Base de Datos:** **AWS RDS (MySQL)** para la aplicación principal y MySQL en EC2 para WordPress.
* **Automatización:** **CloudFormation** (Infraestructura como Código) y **AWS Lambda** para tareas programadas.
* **Seguridad:** VPC con subredes públicas/privadas y **Security Groups** configurados bajo el principio de menor privilegio.
* **Monitorización:** **CloudWatch** y **SNS** para alertas en tiempo real.

---

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

## 👥 Equipo (ASIR2)
- **Alberto Fernández Baeza** - *Administración de Infraestructura & AWS*
- Nicolás Bedia García
- Juan Boo Ruiz
- Raúl Fraile Gándara
- Adrián Romo Oria

---
*Este proyecto es una demostración de competencias en administración de sistemas y arquitectura cloud.*
