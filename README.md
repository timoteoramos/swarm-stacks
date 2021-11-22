# Swarm Stacks

Useful configurations for Docker Swarm.

## Core

The stacks on this repository will assume that you have at least this stack properly configured. You will need to fill some requisites:

```bash
# Public network interface (for Traefik and common services)
docker network create --driver=overlay public

# Frontend node tag: strategy to keep Traefik and HTTP services on the same node (replace $FRONTEND_NODE with a specific node name)
docker node update --label-add frontend=true $YOUR_FRONTEND_NODE
```
