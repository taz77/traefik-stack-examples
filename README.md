# Stack Deployment Examples using Traefik 2.x

At the time of starting this repository, there is a lack of good examples for Traefik 2.x usage. This repository are examples that I have developed for my own use. Most, if not all, of these examples have been run on a Docker Swarm at some point.

When possibly, I prefer to keep all configuration in the Yaml files and rely on configuration files as little as possible - especially with Traefik container itself. I have avoided the use of a TOML file.

In these examples I use the fictitious domain `dev.mytraefik.com` and I use Namecheap for ACME (Let's Encrypt) DNS challenge. For persistent storage I use a NFS version 4 mount with the address of `nas.local`
