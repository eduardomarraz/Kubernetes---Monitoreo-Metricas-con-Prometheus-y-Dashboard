# Proyecto de Monitoreo con Kubernetes: Grafana y Prometheus

Este proyecto despliega dos aplicaciones, Grafana y Prometheus, utilizando Kubernetes. Los archivos YAML proporcionados configuran los pods necesarios para cada aplicación y se pueden aplicar utilizando `kubectl apply`.

## Estructura del Proyecto

```plaintext
..\Programador sistemas en AWS\Kubernetes y Docker\Ejercicios\Kubectl-Monitoreo-main
│
├── kustomization.yaml
├── GRAFANA
│   ├── code_explicacion.md
│   ├── gfn-deployment.yaml
│   ├── gfn-configmap.yaml
│   ├── gfn-hpa.yaml
│   ├── gfn-pv.yaml
│   ├── gfn-pvc.yaml
│   ├── gfn-service.yaml
│   ├── provisioning
│   │   └── datasources.yaml
│   └── kustomization.yaml
│
└── PROMETHEUS
    ├── code_explicacion.md
    ├── prometheus.yaml
    ├── ptheus-configmap.yaml
    ├── ptheus-deployment.yaml
    ├── ptheus-service.yaml
    └── kustomization.yaml
```
<h2>Archivos y Directorios</h2>

### kustomization.yaml
- Archivo principal para la personalización de Kubernetes.

### GRAFANA/
- **code_explicacion.md**: Explicación del código y la configuración.
- **gfn-deployment.yaml**: Define el despliegue de Grafana con sus réplicas y configuración de contenedores.
- **gfn-configmap.yaml**: Configuración de variables de entorno y otros parámetros necesarios.
- **gfn-hpa.yaml**: Configuración de autoescalado horizontal basado en el uso de CPU.
- **gfn-pv.yaml** y **gfn-pvc.yaml**: Configuración de volúmenes persistentes para almacenar datos de Grafana.
- **gfn-service.yaml**: Define el servicio de Grafana para exponerlo dentro del clúster.
- **provisioning/datasources.yaml**: Configuración de fuentes de datos para Grafana.
- **kustomization.yaml**: Personalización específica para Grafana.

### PROMETHEUS/
- **code_explicacion.md**: Explicación del código y la configuración.
- **prometheus.yaml**: Configuración principal de Prometheus.
- **ptheus-configmap.yaml**: Configuración de variables de entorno y otros parámetros necesarios.
- **ptheus-deployment.yaml**: Define el despliegue de Prometheus con sus réplicas y configuración de contenedores.
- **ptheus-service.yaml**: Define el servicio de Prometheus para exponerlo dentro del clúster.
- **kustomization.yaml**: Personalización específica para Prometheus.

## Requisitos

- Kubernetes 1.18+
- kubectl configurado para interactuar con tu clúster de Kubernetes

## Despliegue

Para desplegar las aplicaciones en tu clúster de Kubernetes, sigue estos pasos:

1. Clona el repositorio a tu máquina local:
    ```sh
    git clone <URL-del-repositorio>
    cd Kubectl-Monitoreo-main
    ```

2. Aplica los archivos de configuración utilizando `kubectl apply`:
    ```sh
    kubectl apply -k .
    ```

## Explicación de los Archivos de Configuración

### Grafana

- `gfn-deployment.yaml`: Define el despliegue de Grafana con sus réplicas y configuración de contenedores.
- `gfn-configmap.yaml`: Configuración de variables de entorno y otros parámetros necesarios.
- `gfn-hpa.yaml`: Configuración de autoescalado horizontal basado en el uso de CPU.
- `gfn-pv.yaml` y `gfn-pvc.yaml`: Configuración de volúmenes persistentes para almacenar datos de Grafana.
- `gfn-service.yaml`: Define el servicio de Grafana para exponerlo dentro del clúster.
- `provisioning/datasources.yaml`: Configuración de fuentes de datos para Grafana.

### Prometheus

- `prometheus.yaml`: Configuración principal de Prometheus.
- `ptheus-configmap.yaml`: Configuración de variables de entorno y otros parámetros necesarios.
- `ptheus-deployment.yaml`: Define el despliegue de Prometheus con sus réplicas y configuración de contenedores.
- `ptheus-service.yaml`: Define el servicio de Prometheus para exponerlo dentro del clúster.

## Referencias

- [Documentación de Kubernetes](https://kubernetes.io/docs/home/)
- [Documentación de Grafana](https://grafana.com/docs/)
- [Documentación de Prometheus](https://prometheus.io/docs/)

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para discutir cualquier cambio.

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo `LICENSE` para más detalles.
