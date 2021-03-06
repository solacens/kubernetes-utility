# Kubernetes Utility

> Easier Access on Kubernetes

### Introduction

This tool is aim to provide easier access on Kubernetes funtionalities like:

- Context switch
- Namespace preference
- Pods access like `kubectl logs -f` and `kubectl exec -it`
- `kubetail` that provides combination of pods' log
- Recent history of commands

### Installation

We provide easy installation with [`brew`](https://brew.sh/) + [`brew cask`](https://caskroom.io)

```bash
# You may need to tap something first
brew tap johanhaleby/kubetail
brew tap solacens/brew

# Install it
brew cask install kubernetes-utility
```

### Usage

- The application will take Kubernetes config at `~/.kube/config` by default
- The application will take AWS config at `~/.aws/` by default for supporting EKS authenication if necessary
- The application will not take `KUBECONFIG` environment

```bash
# Tips to merge all files in KUBECONFIG env

# Backing up existing config
mv ~/.kube/confg ~/.kube/config.back

# Write merged config to default path
kubectl config view --flatten > ~/.kube/confg
```