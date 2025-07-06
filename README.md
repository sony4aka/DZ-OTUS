инструкция по запуску приложения
1.Установка БД posgresql - helm install postgresql bitnami/postgresql -f helm/postgresql/values.yaml

2.Применить манифесты в след порядке:
kubectl apply -f kubernetes/db-secret.yaml
kubectl apply -f kubernetes/app-configmap.yaml
kubectl apply -f kubernetes/deployment.yaml
kubectl apply -f kubernetes/service.yaml
kubectl apply -f kubernetes/ingress.yaml
kubectl apply -f kubernetes/db-migration-job.yaml
