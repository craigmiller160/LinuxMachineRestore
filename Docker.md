# Install Docker

Installing Docker should be done before setting up Kubernetes.

## Repository Dependencies

Ensure that the following dependencies are installed:

```
sudo apt update
sudo apt install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```

## Docker GPG Key

Add the Docker GPG Key:

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

## Docker Repository

Add the Docker Repository:

```
echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

## Install Docker

```
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
```