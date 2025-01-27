# KubernetesProject
# Κατεβάζουμε τα 4 yaml αρχεία και τα αποθηκεύουμε σε καποιο directory.

# ubuntuVm terminal:
minikube start # To minikube θα δημιουργησει μια τοπικη συσταδα Kubernetes
minikube status # Ελέγχουμε οτι το Minikube λειτουργεί
cd /path/to/direcotry

# Εφαρμόζουμε τα αρχεία yaml για να αναπτύξουμε τις εφαρμογές:
kubectl apply -f multiplication-app-deployment.yaml
kubectl apply -f nginx-deployment.yaml
kubectl apply -f multiplication-app-service.yaml
kubectl apply -f nginx-service.yaml

# Ελέγχουμε οτι τα deployments και τα services λειτουργούν:
kubectl get deployments
kubectl get pods
kubectl get services

# Πρόσβαση στις εφαρμογές
minikube ip # Κρατάμε τον αριθμό
kubectl get services #Κρατάμε τους αριθμούς αμέσως πριν το /TCP

# Απο τα αποτελεσματα των δύο παραπάνω εντολών βρίσκουμε τη διεύθυνση για τις εφαρμογές
# Παράδειγμα
curl http://192.168.58.2:32233
# και
curl http://192.168.58.2:32233
