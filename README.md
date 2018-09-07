# Pods Exercises

This collection of pods and exercises have been modified starting from the
[Craft kubernetes
workshop](https://github.com/kelseyhightower/craft-kubernetes-workshop) of
Kelsey Hightower.

## Preparation

* Start minikube or Kubernetes for mac

## Deploy first Pod

* Have a look at `podTemplates/monolith.yaml`
* `kubectl apply -f podTemplates/monolith.yaml`
* `kubectl port-forward monolith 10080:80`

Endpoints:

http://127.0.0.1:10080/login
http://127.0.0.1:10080/secure

---

## Deploy second Pod

* Have a look at `podTemplates/healthy-monolith.yaml`
* `kubectl apply -f podTemplates/healthy-monolith.yaml`
* `kubectl port-forward healthy-monolith 10081:81`

Endpoints:

http://127.0.0.1:10081/readiness/status
http://127.0.0.1:10081/healthz/status
