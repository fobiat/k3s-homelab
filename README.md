## **A kubernetes k3s cluster powered by FluxV2 and Github actions.**

****Version 2*** - currently single node due to unaffordable electric costs in the UK (68.3p/kwh) (see [deprecated k8s cluster running on Dell Poweredge)](https://github.com/fobiat/k8s-gitops)* <br />
**Member of the k8s-at-home community**  
**Github -** https://github.com/k8s-at-home  
**Repos -** https://github.com/k8s-at-home/awesome-home-kubernetes  
**Discord -** https://discord.gg/RGvKzVg


## Hardware
- This kubernetes ~~cluster~~ node is currently run on a Dell Optiplex 3050 SFF with 4 Cores and 8 Threads and 32gb RAM.
- Proxmox for the hypervisor with a Ubuntu Server 20.04lts VM with 500gb nvme boot drive and a 240gb SSD scratch drive for downloading and unzipping before moving to a 24TB pool running on a synology NAS for backups and media storage.
- HP Microserver gen 8 (i3-3240T, 16gb ram) runs Proxmox for the hypervisor for a pi-hole LXT and a opnsense VM for the router.
 

 - List item

| Node              | Specification                                        |
| ----------------- | ---------------------------------------------------- |
| k1.resolv.sh      | 4 Cores, 32gb, 20.04LTS, control-plane,master,worker |
| k2-arm64.resolv.sh| **[WIP]** Raspberry pi 4 8gb, ARM64 tainted worker   |



## Packages

This cluster uses a number of tools to work properly:

* Kubernetes k3s - Production-Grade Container Orchestration,
	automated container deployment, scaling, and management.
* K3sup- Uses Ansible to deploy a lightweight k3s production ready cluster.
* Containerd - An industry-standard container runtime with an emphasis on simplicity, robustness and portability.
* Flux2 - Open and extensible continuous delivery solution for Kubernetes. Powered by GitOps Toolkit.
* Github - Code hosting platform for version control and collaboration.
* Github actions - CI/CD runner for workflows
* Calico - an open source networking and network security solution for containers.
* ~~MetalLB - load-balancer implementation for bare metal Kubernetes clusters.~~
* 
## To Do 
*Very much a work in progress, It'll be finished over the coming months. Subject to change.*
 * [x] K3s/k3sup bootstrap
 * [x] Calico network manage for interpod networking
 * [x] Traefik for reverse proxy and ingress
 * [ ] Cloudflare DDNS
 * [ ] Cloudflare tunnels for service exposure to the web
