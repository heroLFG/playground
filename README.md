# playground

- http://localhost:30011 - rocketchat
- https://localhost:30012 - k8s-dashboard
- http://localhost:30000 - prometheus
- http://localhost:32000 - grafana

## argocd does gitops and deploys from this repo
`kubectl port-forward svc/argocd-server -n argocd 8080:80`

## learning

- k8s on docker for windows is limited
  - unable to do traefik load balancing with the default k8s which comes with docker for windows
    - https://docs.docker.com/desktop/kubernetes/
      - `The Kubernetes server runs locally within your Docker instance, is not configurable, and is a single-node cluster`
- minikube can be used to create k8s clusters with different versions: https://minikube.sigs.k8s.io/docs/start/
  - `minikube start -p aged --kubernetes-version=v1.16.1`
