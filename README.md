## Source

[visitors-operator](https://github.com/kubernetes-operators-book/chapters)

## Run operator locally

```
kubectl apply -f deploy/crds/example.com_visitorsapps_crd.yaml
kubectl apply -f deploy/crds/example_v1_visitorsapp_crd.yaml
export OPERATOR_NAME=visitors-operator
operator-sdk run --local
kubectl apply -f deploy/crds/example_v1_visitorsapp_cr.yaml
kubectl apply -f deploy/crds/example.com_v1_visitorsapp_cr.yaml
```

## Run operator on kubernetes

```
cd visitors-operator
kubectl apply -f deploy/crds/example.com_visitorsapps_crd.yaml
kubectl apply -f deploy/crds/example_v1_visitorsapp_crd.yaml
cd deploy
kubectl apply -f .
kubectl apply -f deploy/crds/example_v1_visitorsapp_cr.yaml
kubectl apply -f deploy/crds/example.com_v1_visitorsapp_cr.yaml
# open http://192.168.49.2:30686/
```

## Build image

```
operator-sdk build <image_name>
```
