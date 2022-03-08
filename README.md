# playground

- http://localhost:30011 - rocketchat
- https://localhost:30012 - k8s-dashboard
- http://localhost:30000 - prometheus
- http://localhost:32000 - grafana
- http://localhost:30080 - gogs
- http://localhost:30002 - harbor

## argocd does gitops and deploys from this repo
`kubectl port-forward svc/argocd-server -n argocd 8080:80`

## learning

- k8s on docker for windows is limited
  - unable to do traefik load balancing with the default k8s which comes with docker for windows
    - https://docs.docker.com/desktop/kubernetes/
      - `The Kubernetes server runs locally within your Docker instance, is not configurable, and is a single-node cluster`
- testing with older versions of k8s
  - minikube can be used to create k8s clusters with different versions: https://minikube.sigs.k8s.io/docs/start/
    - `minikube start -p aged --kubernetes-version=v1.16.1`
  - https://microk8s.io/docs/setting-snap-channel
  - with kind:
    - https://stackoverflow.com/questions/56046451/use-kind-to-install-different-kubernetes-version
    - `kind create cluster --image "kindest/node:v1.14.1"`
      - https://hub.docker.com/r/kindest/node/tags
- instead of ngrok:
  - https://jerrington.me/posts/2019-01-29-self-hosted-ngrok.html
