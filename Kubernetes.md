# Kubernetes Cluster

This is about restoring the Kubernetes cluster.

## Create Authcode Directory

Create this directory to support refreshing the TLS cert:

```
mkdir -p /home/craig/authcode
```

## Clone and Follow Main Cluster Repo

This repo has most of the instructions necessary for the restoration. Once it is cloned, follow the instructions inside. Of course, all the individual application repos will need to be cloned too.

<a href="https://github.com/craigmiller160/LocalKubernetesDeployment">Local Kubernetes Deployment</a>

## Setup Kubernetes Auto-Complete

Add this to the `.bash_profile`:

```
# Kuberentes Auto-Complete
source <(kubectl completion bash)
```

## Setup Kubernetes Drive (Eventually)

At some point I really need to setup a dedicated K8s drive so that I don't have to restore the drive each time. I'm not going to detail restore instructions, only because it's a mess.