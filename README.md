# Knative Katas

This repository contain exercises for [Knative](https://knative.dev), a platform
for building event-driven serverless applications.

Knative runs on top of Kubernetes and these exercises assume access to a
Kubernetes cluster with Knative deployed.

Since network access to clusters vary, exercises use the following environment
variables to define how to access the cluster network. Adjust these as necessary
for your cluster.

```console
export KATAS_DOMAIN=example.com
export KATAS_PROTOCOL=https
export KATAS_NAMESPACE=default
```

Some of the exercises make use of the `kn` and `stern` tools. You can either
install these locally, or use the scripts in this repository for a
container-based solution:

```console
alias kn=scripts/kn.sh
alias stern=scripts/stern.sh
```

## Exercises

### Knative Serving

- [Blue/green and Canary Deployments](blue-green-and-canary.md)
- Header-based Revision Routing
- Configuring and Optimizing Autoscaling
- [:construction: WIP: Using gRPC](using-grpc.md)

### Knative Eventing

- [Source to Sink](source-to-sink.md)
- [Custom Sources](custom-sources.md)
- Channels and Subscriptions
- [Brokers and Triggers](brokers-and-triggers.md)
- [Flows - Parallels and Branches](parallels-and-branches.md)
- Flows - Sequences
- [Delivery Errors - Dead Letter Sinks](delivery-errors.md)
- Delivery Errors in Flows
- [:construction: WIP: Kafka Source and Source](kafka-sink-source.md)
- [:construction: WIP: Kafka Broker](kafka-broker.md)
- [:construction: WIP: Kafka Partitions, Cloudevent `partitionKey` and Scalability](kafka-partitions.md)

### Third Party Integrations

- Third Party Sources
- Metrics with Prometheus and Grafana
- Event Tracing with Jaeger

### Misc

- [:construction: WIP: Debugging Techniques](debugging.md)

### Event Delivery Models Overview

![Delivery Models](images/event-delivery-models.png)

### Links

- [Knative reference](https://knative.dev/docs/reference/)
- [Knative Runtime Contract](https://github.com/knative/specs/blob/main/specs/serving/runtime-contract.md)
- [Istio katas](https://github.com/MichaelVL/istio-katas)