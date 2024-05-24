# SnapDrop on Kubernetes
This repo is my version of SnapDrop for my int.kdedesign.nl Kubernetes cluster.

How to build the images:
```
git clone https://github.com/RobinLinus/snapdrop.git snapdrop
podman build --tag ghcr.io/kdeenkhoorn/snapdrop-nginx:latest -f Dockerfile-nginx .
podman build --tag ghcr.io/kdeenkhoorn/snapdrop-node:latest -f Dockerfile-node .
podman push ghcr.io/kdeenkhoorn/snapdrop-nginx:latest
podman push ghcr.io/kdeenkhoorn/snapdrop-node:latest
```

How to start:
```
kubectl apply -f snapdrop/create_deployment_snapdrop
```

Have fun!

Kl@@s

