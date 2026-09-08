# Example Deployment nginx 

## Prepare 

```
cd
mkdir -p manifests 
cd manifests 
mkdir 03-deploy 
cd 03-deploy 
nano nginx-deployment.yml 
```

```
# vi nginx-deployment.yml 
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  selector:
    matchLabels:
      app: nginx
  replicas: 8 # tells deployment to run 8 pods matching the template
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginxinc/nginx-unprivileged:1.28
        ports:
        - containerPort: 8080
        
```

```
kubectl apply -f . 
```

## Explore 

```
kubectl get all
```

## Optional: Change image - Version 

```
nano nginx-deployment.yml 
```


### Version 1: (optical nicer)

```
# Ändern des images von nginxinc/nginx-unprivileged:1.28 -> auf 1.29
# danach 
kubectl apply -f . && watch kubectl get pods 
```

### Version 2: 

```
# Ändern des images von nginxinc/nginx-unprivileged:1.28 -> auf 1.29
# danach 
kubectl apply -f . && kubectl get all && kubectl get pods -w
```
### Version 3 mit Deployment 

```

# vi nginx-deployment.yml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-nfs
spec:
  selector:
    matchLabels:
      app: nginx-nfs
  replicas: 8 # tells deployment to run 8 pods matching the template
  template:
    metadata:
      labels:
        app: nginx-nfs
    spec:
      containers:
      - name: nginx-nfs
        image: nginx:1.28
        ports:
        - containerPort: 8080
        command:
        - "/bin/bash"
        - "-c"
        - set -euo pipefail; while true; do echo $(hostname)$(date) >> /mnt/nfs/outfile; sleep 1; done
        volumeMounts:
        - name: persistent-storage
          mountPath: "/mnt/nfs"
          readOnly: false
      volumes:
      -   name: persistent-storage
          persistentVolumeClaim:
            claimName: pvc-nfs-dynamic
```
