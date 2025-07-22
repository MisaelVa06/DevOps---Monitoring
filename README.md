# 📈 Sistema de Monitoreo con Prometheus, Grafana, Node Exporter y cAdvisor

Este proyecto implementa un stack de monitoreo para observar métricas del sistema operativo y contenedores Docker en un entorno local.

Forma parte de la **Fase 4 del proyecto DevOps Nivel 1** y permite visualizar en tiempo real el estado del servidor y de los servicios desplegados.

---

## 🧰 Tecnologías utilizadas

|  Herramienta   |                      Rol                       |
|----------------|------------------------------------------------|
| Docker Compose | Orquestación de los contenedores               |
| Prometheus     | Recolección de métricas                        |
| Grafana        | Visualización de métricas en dashboards        |
| Node Exporter  | Exportación de métricas del sistema            |
| cAdvisor       | Exportación de métricas de contenedores Docker |

---

## 📁 Estructura del proyecto

monitoring/

      ├── docker-compose.monitoring.yml

      └── prometheus/
                   └── prometheus.yml


---

## 🚀 Despliegue

### 1. Clonar el repositorio

    git clone https://github.com/Misaelva06/devops-monitoring.git
    cd devops-monitoring
    
2. Levantar los servicios

       docker compose -f docker-compose.monitoring.yml up -d

--- 
 
## 🔍 Acceso a los servicios

Servicio	URL por defecto

    Prometheus	      http://localhost:9090
    
    Grafana          	http://localhost:3000
    
    Node Exporter	    http://localhost:9100/metrics
    
    cAdvisor	        http://localhost:8080

--- 

## 📊 Dashboards disponibles en Grafana

    Puedes importar estos dashboards en Grafana desde la sección "+" → Import:

          Dashboard	                                ID en Grafana
    Node Exporter Full	                            1860
    Docker Monitoring (cAdvisor)	                    193
--- 
## 🧠 Notas adicionales
    
  - La carpeta grafana_data se define como volumen persistente para conservar dashboards entre reinicios.

  - El stack está pensado para ejecutarse en el servidor destino (vm-web) como parte de un flujo automatizado desde vm-control.

--- 
## 📄 Licencia
-  Este proyecto es parte del portafolio de aprendizaje de Misael Vasquez con fines educativos y profesionales.


