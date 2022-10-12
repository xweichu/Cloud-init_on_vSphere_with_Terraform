# Cloud-init on vSphere with Terraform
## Introduction
This tool is used to configure a cluster of VMs on vSphere with Terraform by leveraging Linux Cloud Images (ova) and [Cloud-init](https://cloud-init.io/). This tool focuses on provisioning the infrastructure and adding users accesses (ssh & password). Once the cluster is up and running, other deployment automation tools like [Ansible](https://www.ansible.com/) can be used to further configure the cluster. 

The following Linux Cloud Images have been tested:
- Ubuntu 18.04
- Ubuntu 20.04
- Ubuntu 22.04
- Ubuntu 22.10

## Installation
The tool is tested on Ubuntu 18.04 and 20.04. The following dependencies are need to run this tool:
- Terraform
- whois

You can install the dependencies manually or run the following bash script (besides above dependencies, the script also installs ansible and sshpass). 
```bash
bash ./env_prep.sh
```
## Usage
- Customize the [terraform.tfvars](https://github.com/xweichu/Cloud-init_on_vSphere_with_Terraform/blob/main/terraform.tfvars) file in this folder by refering the comments.
- Run the bash script.
    ```bash
    bash ./cloud_init.sh
    ```
