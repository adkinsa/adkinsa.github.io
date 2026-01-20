---
title: How to install Docker on Ubuntu 24.04 LTS
date: 2026-01-19 8:00 PM
categories: [Docker]
tags: [docker, linux]
---

This post provides a step-by-step guide on how to install Docker on Ubuntu 24.04 LTS. The official [Docker documentation](https://docs.docker.com/engine/install/ubuntu/){: target="_blank"} outlines several methods for installing Docker on Ubuntu. This guide focuses on installing Docker using the apt repository.

## Prerequisites

### Uninstall conflicting packages

Before installing Docker, ensure that any unofficial packages are removed, as they may conflict with the official Docker packages.

According to the official Docker documentation, the unofficial packages are:

* `docker.io`
* `docker-compose`
* `docker-compose-v2`
* `docker-doc`
* `podman-docker`

Uninstall the conflicting packages with:

```shell
sudo apt remove $(dpkg --get-selections docker.io docker-compose docker-compose-v2 docker-doc podman-docker containerd runc | cut -f1)
```

## Install Docker using the apt repository

### Step 1: Set up the Docker apt repository

The following commands will add Docker's GPG key and the repository to apt sources:

```shell
# Add Docker's official GPG key:
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
Types: deb
URIs: https://download.docker.com/linux/ubuntu
Suites: $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}")
Components: stable
Signed-By: /etc/apt/keyrings/docker.asc
EOF

sudo apt update
```

Example output:

![Screenshot of terminal running commands to set up the Docker apt repository](https://res.cloudinary.com/do8uy1fxa/image/upload/v1768673211/set-up-docker-apt-repository_ckbkjc.png)

### Step 2: Install Docker packages

Next, install the Docker packages by running:

```shell
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Example output:

![Screenshot of terminal running command to install Docker packages](https://res.cloudinary.com/do8uy1fxa/image/upload/v1768673188/install-docker-packages_fkixvx.png)

### Step 3: Add user to Docker group

By default, Docker commands must be run with `sudo`. To run Docker commands without `sudo`, add your user to the Docker group by running:

```shell
sudo usermod -aG docker $USER
```

### Step 4: Verify Docker installation

Lastly, verify that the installation was successful with:

```shell
docker run hello-world
```

Example output:

![Screenshot of terminal running the command docker run hello-world](https://res.cloudinary.com/do8uy1fxa/image/upload/v1768673163/docker-run-hello-world_sfluuf.png)

You have now successfully installed Docker on Ubuntu 24.04 LTS.