# Argo infra personal labs

## Infra applications

Available Applications:

| Applications  | DNS | Username  | Password | Links | Comments |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Ingress-nginx | | | | <https://kubernetes.github.io/ingress-nginx> | |
| ArgoCD |  <http://argo-$env.cloud-diplomats.com> | admin  | get password at init script | <https://argo-cd.readthedocs.io/en/stable>  | |
| Keycloak | <http://identity-$env.cloud-diplomats.com/admin/master/console>  | admin  | password |  <https://www.keycloak.org>  | To activate metrics realmsSettings/events/metrics-listener |
| RabbitMQ  | <http://rabbitmq-$env.cloud-diplomats.com>  | admin  | password | <https://www.rabbitmq.com>  | |
| CertManager | | | | <https://cert-manager.io/> | |
| External Secret Operator | | | | <https://external-secrets.io/latest> | |
| External DNS | | | | <https://kubernetes-sigs.github.io/external-dns/v0.13.6/> | |

## ArgoCD Folders organization

### Applications

#### Base

- **base/shared-app**: Contains cluster-wide infra configurations deployed by the ArgoCD shared application.

#### Overlay

Environments folders that inherit from base folder. It uses [kustomize](https://github.com/kubernetes-sigs/kustomize) to allow environment based customization.

### ArgoCD Applications

#### Base

- **base**: Contains ArgoCD Infra Applications

#### Overlay

Environments folders that inherit from base folder. It uses [kustomize](https://github.com/kubernetes-sigs/kustomize) to allow environment based customization.
