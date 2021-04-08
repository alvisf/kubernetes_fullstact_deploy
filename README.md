# kubernetes_fullstact_deploy

Deployed a full-stack application ( Nginx, Node.js and MongoDB)

Build the Docker Image 🐳

### FrontEnd

```docker build -t frontendvm .```

### BackEnd

```docker build -t backendvm .```

### Database

```docker build -t mongo .```

So now we can scale it with microservice architecture.
we are going to use Docker to containerise our application
Now we can deploy the image as a container and scale it up
we need to create a deployment for the application and service to deliver the application. We will start by creating a deployment from this YAML file we have got.
Create the Deployment and services
Likewise, we can deploy the service from the YAML file.
If you have a Kubernetes service named frontend-service, you can use mongo-service as the DNS name of your application. It’s the responsibility of Kubernetes to forward the request to the corresponding pod.

### FrontEnd
```kubectl apply -f nginx-deployment.yaml```

```kubectl apply -f nginx-service.yaml```

### Backend
```kubectl apply -f server-deployment.yaml```
```kubectl apply -f server-service.yaml```

### Database
```kubectl apply -f mongo-deployment.yaml```
```kubectl apply -f mongo-service.yaml```

