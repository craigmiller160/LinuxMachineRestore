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

## Setup Maven With Nexus

Maven needs to be setup to load dependencies from Nexus.

First, copy the `settings.xml` file to the Maven `.m2` directory:

```
mkdir -p ~/.m2/
cp ~/Development/Applications/LocalKubernetesDeployment/nexus/settings.xml ~/.m2/
```

Then, edit the file and replace the password with the craigmiller160 password for Nexus in 1Password.

## Setup NPM With Nexus

NPM needs to be setup to work with Nexus.

First, setup NPM to pull from the Nexus NPM registry:

```
npm config set registry https://craigmiller160.ddns.net:30003/repository/npm-group/
```

Then, add the craigmiller160 user whose password can be found in 1Password:

```
npm adduser --registry=https://craigmiller160.ddns.net:30003/repository/npm-private/
```

## Setup Docker Environment Variables

Add the following to the `.bash_profile` file, adding in the actual values:

```
# Craig Build Nexus Docker Credentials
export NEXUS_DOCKER_USER=craigmiller160
export NEXUS_DOCKER_PASSWORD=#####
```

## Install Build Tool

The custom build tool needs to be installed for future development.

```
npm i -g @craigmiller160/craig-build
```
