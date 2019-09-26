# architecture

![overview](./overview.svg)

## Local Setup

```bash
minikube start --kubernetes-version v1.15.2
helm init
helm install codecentric/keycloak --name keycloak --wait
```

2. Setup Keycloak

* Create realm `samply`
* Create confidential client `catalog-api`
* Create `seller` role and group
* Create sample seller user
* Add `http://localhost:8080` as web origin to client settings