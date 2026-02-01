# 🎨 Proyecto RETACANTABRIA / Academia de Pintura: Solución Cloud de Alta Disponibilidad

[![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://www.php.net/)

Este proyecto consiste en el diseño e implementación de una infraestructura en la nube para una academia de pintura, priorizando la **alta disponibilidad (24/7)**, la **seguridad** y la **optimización de costes**. Desarrollado como parte del reto **RetaCantabria 2025/2026**.

---
<img src="https://cdn.jsdelivr.net/gh/boyney123/awsicons/src/icons/VirtualPrivateCloud.svg" width="40">VPCNetworkingSegmentación de red con subredes públicas y privadas.<img src="https://cdn.jsdelivr.net/gh/boyney123/awsicons/src/icons/Ec2.svg" width="40">EC2ComputaciónHosting de la aplicación PHP y WordPress (Glosario).<img src="https://cdn.jsdelivr.net/gh/boyney123/awsicons/src/icons/ElasticLoadBalancingApplicationLoadBalancer.svg" width="40">ALB & ASGEscalabilidadBalanceador de carga y auto-escalado para alta disponibilidad.<img src="https://cdn.jsdelivr.net/gh/boyney123/awsicons/src/icons/Rds.svg" width="40">RDS (MySQL)Base de DatosBase de Datos relacional gestionada para la app principal.<img src="https://cdn.jsdelivr.net/gh/boyney123/awsicons/src/icons/SimpleStorageServiceStandard.svg" width="40">S3AlmacenamientoDestino de backups diarios automatizados vía cron.<img src="https://cdn.jsdelivr.net/gh/boyney123/awsicons/src/icons/Lambda.svg" width="40">LambdaAutomatizaciónEjecución de código sin servidores para tareas programadas.<img src="https://cdn.jsdelivr.net/gh/boyney123/awsicons/src/icons/CloudFormation.svg" width="40">CloudFormationIaCDespliegue automático de recursos mediante plantillas YAML.<img src="https://cdn.jsdelivr.net/gh/boyney123/awsicons/src/icons/SimpleNotificationService.svg" width="40">SNSMensajeríaServicio sencillo de notificaciones y alertas.<img src="https://cdn.jsdelivr.net/gh/boyney123/awsicons/src/icons/CloudWatch.svg" width="40">CloudWatchMonitorizaciónMonitorización y observabilidad de todo el sistema cloud.
Auto Scaling Group
Grupos de destino
Sustitución automática de instancias en caso de fallo\



<table align="center">
  <tr>
    <td align="center">
      <img src="Reto_G2_AplicacionPHP.png" alt="App PHP" width="450">
      <br>
      <sub><b>Interfaz Aplicación PHP</b></sub>
    </td>
    <td align="center">
      <img src="Reto_G2_WordPress.png" alt="WordPress" width="450">
      <br>
      <sub><b>Glosario WordPress</b></sub>
    </td>
  </tr>
</table>

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
