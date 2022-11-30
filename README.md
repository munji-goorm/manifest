# manifest
먼지구름 k8s manifest

# 파일 실행 순서
## configmap, secret 생성
kubectl apply -f cfgmap.yaml

kubectl apply -f secret.yaml

kubectl apply -f db-pwds.yaml

## db cluster 생성
kubectl apply -f db-cluster.yaml

## python pod를 통해 db에 값 입력 후 삭제
kubectl apply -f py-once.yaml

kubectl apply -f py-hour-temp.yaml

kubectl apply -f py-day-temp.yaml

kubectl delete po py-once py-hour py-day

## cronjob 생성
kubectl apply -f py-hour.yaml

kubectl apply -f py-day.yaml

## backend service & deployment 생성
kubectl apply -f back-svc.yaml

kubectl apply -f back-deploy.yaml

## frontend service & deployment 생성
kubectl apply -f front-svc.yaml

kubectl apply -f front-deploy.yaml
