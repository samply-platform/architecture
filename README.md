# architecture
![overview](./overview.png)

## Local Setup

```bash
minikube start --kubernetes-version v1.15.2
helm init
helm install --name keycloak \
    --set keycloak.persistence.deployPostgres=true \
    --set keycloak.persistence.dbVendor=postgres \
    codecentric/keycloak --wait
```

### Setup Keycloak

* Create realm `samply`
* Create confidential client `catalog-api`
* Create `seller` role and group
* Create sample seller user
* Add `http://localhost:8080` as web origin to client settings
