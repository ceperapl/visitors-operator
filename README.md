## How to run

```
kubectl apply -f deploy/crds/example.com_visitorsapps_crd.yaml
kubectl apply -f deploy/crds/example_v1_visitorsapp_crd.yaml
export OPERATOR_NAME=visitors-operator
operator-sdk run --local
kubectl apply -f deploy/crds/example_v1_visitorsapp_cr.yaml
kubectl apply -f deploy/crds/example.com_v1_visitorsapp_cr.yaml
```
