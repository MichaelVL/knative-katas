[//]: # (Copyright, Michael Vittrup Larsen)
[//]: # (Origin: https://github.com/MichaelVL/knative-katas)
[//]: # (Tags: #knative-eventing #grpc #blue-green #canary)

# Using gRPC

This exercise demonstrates the use of Knative eventing with gRPC, and we will
demonstrate it using the [sentences](https://github.com/MichaelVL/istio-katas/sentences-app/app-grpc)
application from the [Istio-katas](https://github.com/MichaelVL/istio-katas).

The sentences application consists of a frontend `sentences` and two backends,
`age` and `name`. The frontend communicates with the backends using gRPC.

Deploy the three services:

```console
kubectl apply -f deploy/v1-grpc
```

Next, run the following command to request a sentence:

```console
curl $KATAS_PROTOCOL://sentences.$KATAS_NAMESPACE.$KATAS_DOMAIN
```






## Cleanup

```console
kubectl delete -f deploy/v1-grpc
```
