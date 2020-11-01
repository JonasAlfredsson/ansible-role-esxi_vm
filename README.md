# ansible-role-esxi_vm

This Ansible role will install some additional programs and configurations
that are useful when the targeted machine is a VM running on a [VMware ESXi][1]
host.

> This is currently a very barebone role which will be expanded in the future.



# Installation

This repository does not have any dependencies, so just move into your `roles/`
folder and run the following:

```bash
git clone git@github.com:JonasAlfredsson/ansible-role-esxi_vm.git esxi_vm
```

If you would like to download any updates for this role in the future, you may
use the following command from within the previously cloned folder:

```bash
git pull
```

When the configuration is complete you may then just include this role in your
main playbook like this:

```yaml
- hosts: all
  name: Install extra programs when the machine is a VM on an ESXi host
  roles:
    - esxi_vm
```



# Usage

As of now this roles does not have any configurable options, so you don't have
to do anything else to use this role.



# Additional Information

This section contains additional information that may be good to know when
working with ESXi hosts and their guest systems.


## Login URL
To reach the web UI of a newly installed ESXi server you should try to visit
the following URL:

```
https://<host_ip>/ui/#/login
```


## Download ESXi
The ESXi hypervisor, also known as VMware vSphere Hypervisor, is not the easiest
program to download. A large part of this is because the official VMware
[homepage][2] is really horrible to navigate, so the fasted way I have found
to be able to navigate to the download page for ESXi is to first login to
"[my vmware][3]" and then follow the links found in [this KB article][4].






[1]: https://en.wikipedia.org/wiki/VMware_ESXi
[2]: https://www.vmware.com/
[3]: https://my.vmware.com/
[4]: https://kb.vmware.com/s/article/2107518
