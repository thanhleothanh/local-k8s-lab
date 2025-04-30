## Features

- RKE2, with self-provided secret token
- Kube-VIP for controller planes
- Ingress Nginx Controllers
- Rancher Server for cluster management
- HAProxy and Keepalived VIP

## Configurations

- Remember to change variables in `inventory/group_vars/all.yaml` and `inventory/hosts.ini` according to VMs config
- By default, Ingress Nginx Controllers are exposed behind NodePort service at :30080 and :30443
- By default, HAProxy layer is deployed on the agent servers, but still outside the RKE2 cluster, it can be deployed in separate servers
- By default, Rancher Server is deployed inside the RKE2 cluster, it can be deployed outside of the cluster and on separate servers
