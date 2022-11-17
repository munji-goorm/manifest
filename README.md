# manifest
먼지구름 k8s manifest

# 파일 실행 순서
kubectl apply -f cfgmap.yaml

kubectl apply -f secret.yaml

kubectl apply -f db-pv.yaml

kubectl apply -f db-pvc.yaml

kubectl apply -f db-svc.yaml

kubectl apply -f db-deploy.yaml

kubectl apply -f py-once.yaml

kubectl apply -f py-hour.yaml

kubectl apply -f py-day.yaml

kubectl apply -f back-svc.yaml

kubectl apply -f back-deploy.yaml

kubectl apply -f front-svc.yaml

kubectl apply -f front-deploy.yaml

kubectl delete -f py-once.yaml

kubectl delete -f py-hour.yaml

kubectl delete -f py-day.yaml
