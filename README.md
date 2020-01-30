# Stack Deployment Examples using Traefik 2.x

At the time of starting this repository, there is a lack of good examples for Traefik 2.x usage. This repository are examples that I have developed for my own use. Most, if not all, of these examples have been run on a Docker Swarm at some point.

When possibly, I prefer to keep all configuration in the Yaml files and rely on configuration files as little as possible - especially with Traefik container itself. I have avoided the use of a TOML file.

In these examples I use the fictitious domain `dev.mytraefik.com` and I use Namecheap for ACME (Let's Encrypt) DNS challenge. For persistent storage I use a NFS version 4 mount with the address of `nas.local`

The network `web` is a pre-existing network created on the swarm that is used by Traefik.

The version of Docker Compose Yaml for stack deployment will vary in this repository as I have not went through them all to update and get on the same version.


|  Deployment |  Yaml |
|---|---|
| Traefik 2.x  |  docker-stack-deploy-traefik.yml |
| Nexus V3  | docker-stack-deploy-nexus.yml  |
|   |   |
|   |   |


## Trafik 2.x
The main reason you are here. The Traefik 2.x stack deployment has two containers with the first obviously being Traefik. The second container is used to explor the SSL certificates from the JSON file that Traefik uses to store them to indiviual PEM files with appropriate private keys and chains as necesssary. I have added this because sometimes a container needs to have the certificates being used to encrypt the traffic to the container.