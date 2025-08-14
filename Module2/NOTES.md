# **Module 2: Compute & Networking**

## Compute Services
| Service       | Use Case                      | Example CLI Command                      |
|---------------|-------------------------------|------------------------------------------|
| Virtual Machines | Lift-and-shift workloads   | `az vm create --name MyVM --image UbuntuLTS` |
| App Services  | Web apps with auto-scaling    | `az webapp create --name MyApp --plan MyPlan` |

## Networking Components
- **Virtual Network (VNet)**: Private network in Azure
- **Load Balancer**: Distributes traffic across VMs
- **VPN Gateway**: Connects to on-premises networks

## Exercise Notes
- Created VM with NGINX using:
  ```bash
  az vm extension set --publisher Microsoft.Azure.Extensions \
  --name CustomScript --version 2.0 --vm-name MyVM \
  --settings '{"commandToExecute":"apt-get install nginx -y"}'
