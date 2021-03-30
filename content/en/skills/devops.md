+++
title = "DevOps"
subtitle = "Experience: 2 years"
tags = ['System']
date = 2020-03-27

# For description meta tag
description = "DevOps tools I worked with."

# Comment next line and the default banner wil be used.
banner = 'img/devops.svg'

+++

My DevOps experience is centered around the needs of a company that developed a platform for marketplace integration (Ozon, Wilberries, Tmall, Yandex.Market и Goods).

# Kubernetes

Initially, the company's infrastructure was based on [Docker Compose](https://docs.docker.com/compose/)/[Swarm](https://docs.docker.com/engine/swarm/), but, at some point, switching to Kubernetes became a reasonable option. For K8s deployments I used [Kubespray](https://kubespray.io/) and [K3s](https://k3s.io/).

I faced a number of problems when switched to a cluster-based development, in particular, with local deployments. I tried to organize it using local miniclusters ([kind](https://kind.sigs.k8s.io/), [minikube](https://minikube.sigs.k8s.io/docs/)) with tools like [Tilt](https://tilt.dev/) and [Skaffold](https://skaffold.dev/), but, in the end, for a number of reasons, returned to Compose.

Nevertheless, packaging applications in [Helm charts](https://helm.sh/) somewhat simplified their management in the cloud. To address the issue of a cluster configuration reproducibility at the application level, I tried [Helmfile](https://github.com/roboll/helmfile) and [Helm Terraform provider](https://registry.terraform.io/providers/hashicorp/helm/latest/docs), and settled on the latter.

# CI/CD

In CI/CD my experience is limited to [GitLab](https://docs.gitlab.com/ee/ci/) and [Drone](https://www.drone.io/). For each project that was supposed to be used in production, a pipeline was set up, which included running the code through linters and running all tests, building a new Docker image and deploying this image on the staging and, later, on the production servers. A built-in GitLab registry was used for Docker images. Dockerfiles have been optimized for building a production image.

I became interested in Drone when I discovered that GitLab workers can easily consume 10GB of RAM per **one** worker. But, at some point, it became possible to cheaply move GitLab to a separate server with a bunch of RAM, so the option with Drone has lost its relevance.

# FaaS

The ability to have a FaaS service in your own cluster opens up interesting architectural possibilities. [OpenFaaS](https://www.openfaas.com/) turned out to be a great option, which is quite easy to write functions for. There were problems with local deployment (without a cluster), but an internal development server resolved the issue.

# Nix

Another interesting idea that I have been working on lately is declaratively configurable Linux distributions. They can be used as base systems that are not (so) scary to update. Today, [NixOS](https://nixos.org/) is the only serious contender in this field (not [Guix](https://guix.gnu.org/), unfortunately). I maintain my system configuration in the [git repo](https://git.sr.ht/~alekfed/nix-config/tree), but it would be interesting to try this system for larger tasks.

(see also [system administration card](/skills/linux_bsd))

___
# Illustration

- Title: [AWS](https://aws.amazon.com/) logo. I sometimes look at their web services solutions when working on infrastructure issues. It's a pity that sometimes their prices are so high.

- Infrastructure visualization in the form of "floating boxes": I probably decided to do something similar by looking at the [ELK](https://www.elastic.co/what-is/elk-stack) and [Vault](https://www.hashicorp.com/products/vault). The logos near the layers speak for themselves: with HCL scripts we provide machine configurations ([Terraform](https://www.terraform.io/)), with playbooks—system configurations ([Ansible](https://www.ansible.com/)), with resources—clusters ([Kubernetes](https://kubernetes.io/)), with charts—applications ([Helm](https://helm.sh/)). It should be noted that sometimes the boundaries between layers are not so strict: for example, as mentioned above, Terraform's HCL scripts may as well describe the configuration of Kubernetes clusters at the Helm chart level.

- The logos on the Helm layer: using charts, it's relatively painlessly to deploy a router with automatic TLS ([Traefik](https://traefik.io/traefik/)), a secrets storage with keys autorotation ([Vault](https://www.hashicorp.com/products/vault)), a feature-rich environment for source code ([GitLab](https://gitlab.com/)), and then collect all the needed metrics for [Prometheus](https://prometheus.io/).
