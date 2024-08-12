# [daytona-backstage-demo](https://backstage.io)

This is your newly scaffolded Backstage App. Follow the below steps to get started.

1. Create a new client in Daytona Keycloak by importing [backstage.json](./kc-backstage.json).
2. Update the newly created Daytona client ID and secret in [app-config.yaml](./app-config.yaml).
3. Update the Daytona app domain URL in [app-config.yaml](./app-config.yaml).
4. Run `yarn install` to install the required libraries.
5. Run `yarn dev` to start the development server.

**Note**: Make sure you have updated the Daytona watkins ingress with the below CORS configuration.

```yaml
    nginx.ingress.kubernetes.io/cors-allow-credentials: "true"
    nginx.ingress.kubernetes.io/cors-allow-headers: Authorization, Access-Control-Allow-Origin, Access-Control-Allow-Headers, Origin, Content-Type, Accept, X-Requested-With
    nginx.ingress.kubernetes.io/cors-allow-methods: PUT, GET, POST, OPTIONS, DELETE
    nginx.ingress.kubernetes.io/cors-allow-origin: https://<backstage-app-url>, https://<daytona-domain-url>
    nginx.ingress.kubernetes.io/enable-cors: "true"
```
