# wordpress-building
Build wordpress in kubernetes in ubuntu

  mkdir kubernetes
  cd kubernetes/
  code mysql-deployment.yaml
  cod wordpress-deployment.yaml
  code wordpress-deployment.yaml
  cat <<EOF >>./kustomization.yaml
  resources:
    - mysql-deployment.yaml
    - wordpress-deployment.yaml
  EOF
  m kubectl apply -f .
  m kubectl get secrets
  m kubectl get pods
  cat <<EOF >./kustomization.yaml
  secretGenerator:
  - name: mysql-pass
    literals:
    - password=YOUR_PASSWORD
  EOF
  cat <<EOF >>./kustomization.yaml
  resources:
    - mysql-deployment.yaml
    - wordpress-deployment.yaml
  EOF
  m kubectl delete -f .
  kubectl apply -k ./
  m kubectl get secrets
  m kubectl get pvc
  m kubectl get pvc -w
  m kubectl get pvc
  m kubectl get secrets
  m kubectl get pvc
  m kubectl get storageclass
  m kubectl get pvc
  m kubectl delete -f .
  m kubectl get pvc
  kubectl apply -k ./
  m kubectl get pvc
  m kubectl get pods
  m kubectl get services
  m kubectl get service wordpress
  m kubectl get service wordpress --url
  m kubectl service wordpress --url
  m service wordpress --url
  m kubectl service wordpress
  m kubectl get service wordpress