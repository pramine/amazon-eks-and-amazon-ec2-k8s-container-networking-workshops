---
title: "Oregon"
chapter: false
disableToc: true
hidden: true
---

```
kops create cluster \
  --name=kops-cluster.k8s.local \
  --master-count=1 \
  --master-size=t2.small \
  --node-count=2 \
  --node-size=t2.small \
  --network-cidr=10.0.0.0/16 \
  --zones=us-west-2a,us-west-2b,us-west-2c \
  --ssh-public-key=~/.ssh/id_rsa.pub \
  --networking=kubenet
```
