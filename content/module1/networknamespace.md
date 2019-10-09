---
title: "1. Create a network namespace in Cloud9 host"
chapter: false
weight: 17
---

#### Introduction

1. Open two terminals in the Cloud9 environment. Let's refer them as Terminal 1 and Terminal 2.

2. Terminal 1 is referenced as the `Container Terminal` and Terminal 2 is the `Host Terminal`.


#### Create a network namespace in Terminal 1 (Container) using `unshare`

1. Check docker and network status
```
sudo bash
service docker status
ifconfig -a
```
2. Use unshare to create a mini-container with a separate network namespace

```
unshare --net --fork bash
```

3. Observe processes within the new namespace

```
ps
ifconfig -a
```