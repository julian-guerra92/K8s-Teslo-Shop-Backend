# K8s-Teslo-Shop-Backend

Configuración básica para creación de contenedor mediante el uso de kubernetes y minikube. Para su uso asegurarse de seguir las siguientes indicaciones:

1. Contar con la instalación de mikube para su sistema operativo correpsondiente:
   [URL de Sitio Oficial minikube](https://minikube.sigs.k8s.io/docs/start/)

2. Asegurarse de contar con la instalación de kubectl. Se puede usar el siguiente comando para su verificación:

```
kubectl version
```

3. Iniciar contenedor de minikube mediante el siguiente comando:

```
minikube start
```

4. Agregar los archivos de secrets, configuración y servicios correspondiete (y en este orden) mediante el siguiente comando:

```
kubectl apply -f <ejemplo:postgres-secrets.yml>
```

5. Algunos comandos a tener en cuenta:
- Obetener información del cluster: ```kubectl get all```
- Para ver información de algún Pod en el cluster: ```kubectl describe <ejemplo:deployment.apps/postgres-deployment>```
- Para ver los logs de un servicio del cluster: ```kubectl logs <ejemplo:pod/postgres-deployment-55bcdfbb57-lvjl6>```
- Para reiniciar el deplyment de algún servicio del cluster: ```kubectl rollout restart deployment <ejemplo:backend-deployment>```
- Para abrir y visualizar el servivio desplegado: ```minikube service <ejemplo:pg-admin-service>```
- Limpiar cluster: ```minikube delete --all```
