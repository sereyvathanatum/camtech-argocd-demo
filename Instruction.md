Deploy a simple web application using a Deployment and expose it using a Service.

Instructions:

Create a Deployment manifest (deployment.yaml)

Apply the Deployment:

```
kubectl apply -f deployment.yaml
```

Check Pods and Deployment status:

```
kubectl get pods (You should see two Pods being created)
kubectl get deployments
```

Create a Service manifest (service.yaml):

Apply the Service:

```
kubectl apply -f service.yaml
```

Check Service status and access the app:

```
kubectl get services (Note the PORT(S) column, which shows 80:<NodePort>/TCP).
minikube service my-web-app-service (or find the node IP and NodePort manually)
```

Open the URL in your browser. You should see the Nginx welcome page.
