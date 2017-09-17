| Variable Name | Usage                                                                                                         | Example       |
|---------------|---------------------------------------------------------------------------------------------------------------|---------------|
|		| General variables												|		|
| db_size       | Sets the size of the volume that will be used for Docker storage.  Will be renamed in future version. Integer | 20            |
| db_vol_name   | Name of the Docker storage volume.  Basic string.                                                             | docker_vol    |
| master1       | If using static IPs, set the address of the first master.  Supported in RHV & VMware.                         | 192.168.1.100 |
| node1		| If using static IPs, set the address of the first node. Supported in RHV & VMware.				| 192.168.1.101 |
| node2         | If using static IPs, set the address of the second node.  Supported in RHV & VMware                           | 192.168.1.102 |
| mask          | Used to set the netmask when using static IPs									| 255.255.255.0 |
| gateway       | Used to set the gateway when using static IPs									| 192.168.1.1   |
| domain        | This will be the domain suffix using in the nodes' FQDN							| example.com   |
| dns           | DNS server address that will be populated in resolv.conf if using static IP address				| 192.168.1.10  |
| ssh_user      | The user that will ssh into the OCP VMs to perform post-provisioning activities				| root          |
| vm_name	| The name of VMs.  By default, every VM provisioned will have a 4 digit unique id appended to it's name.	| ocp-master-1  |
| cf_ssh_pass   | The password used to SSH into VMs for post deploy config.  Will be renamed in a future version.               | password      |
| cf_db_dev     | The device name in the OS of the volume that will be used for docker storage.  Will be renamed later.		| /dev/sdb      |
| 		| OpenStack Specific Variables											|		|
| osp_url	| The URL of the OpenStack horizon endpoint									| http://192.168.1.40:5000/v2.0 |
| osp_ip	| The IP of the OpenStack endpoint. 										| 192.168.1.40  |
| osp_user	| The user used to authenticate to OpenStack									| admin		|
| osp_pass	| The password used to authenticate to OpenStack								| password	|
| osp_project	| The project/tenant to deploy OpenStack instances into								| tenant1	|
| az		| The OpenStack availability zone to deploy instances into							| nova		|
|		| VMware specific variables											|		|	
| vcenter_ip    | The IP or FQDN of the vCenter server when using VMware as the host platform					| 192.168.2.5   |
| vcenter_user  | The user account used to authenticate to vcenter								| admin 	|
| vcenter_pass  | The password used to authenticate to vcenter									| password	|
| esx_host	| The specific ESX host used to deploy a node to.  Will add support for DRS clusters at some point.		| esx1		|
| vc_datacenter | The datacenter object to deploy VM(s) to.									| DC1		|
| vc_datastore  | The datastore VMs and their disks will be created in.  Can be unique for each disk/VM				| datastore1    |
| template_name | The name of the template you will be provisioning from.  Works with VMware & RHV				| ocptemplate   |
| network_name  | The name of the virtual network to attach OCP VMs to.  Works with VMware & RHV				| vm_network    |
| 		| Red Had Virtualization/Ovirt specific variables								|		|
| datastore	| The name of the RHV datastore to provision disk to.  Will refactor to combine this and vc_datastore later.    | datastore1    |
| cluster	| The name of the RHV cluster to deploy VMs to.  								| Default  	|
| rhvm_addr	| The FQDN/IP of the RHV manager for provisioning RHV instances.						| 192.168.2.6	|
| rhv_user	| The user to authenticate to RHV										| admin@internal |
| rhv_password	| The password to authenticate to RHV										| password	|
|		| Red Hat subscription manager variables									|		|
| rhn_user	| The user to register VMs to Red Hat subscription manager							| rhn-user	|
| rhn_pass	| The password to register VMs to RH subscriptioin manager							| password	|
| rhn_pool	| The pool used to attach subscription to VMs to RH subscription manager					| N/A		|
|		| IPA/Identity Management Variables										|		|
| ipa_server	| Used to join nodes to IPA/IdM.  										| idm1.jr.int	|
| ipa_user	| User account used to join nodes to IdM									| admin		|
| ipa_password	| Password used to join nodes to IdM										| password	|
