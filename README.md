# MINILAB (Game of Active Directory)

The MINILAB lab by [Orange Cyberdefense](https://github.com/Orange-Cyberdefense/GOAD): one domain with a Windows Server 2019 domain controller and a Windows 10 workstation.
This repository runs it with [Isoloom](https://www.isoloom.com): [`isoloom.yml`](isoloom.yml)
describes the machines (on GOAD's own boxes), and GOAD's own Ansible playbooks build the lab from
a controller.

## Run it

```bash
isoloom generate
cd .isoloom/vagrant && vagrant up
```

About 7.8 GB of memory (`isoloom resources`) plus 1 GB for the controller. Lab guide: the
[GOAD documentation](https://orange-cyberdefense.github.io/GOAD/).

**Tested:** built end to end on VirtualBox (KINGSLANDING, the Windows 10 workstation and the
controller), 0 failed tasks: the domain, the workstation's domain join, and GOAD's
vulnerabilities. The Windows 10 box can drop WinRM briefly during a reboot; re-running
provisioning (`vagrant provision isoloom-controller --provision-with ansible`) completes it.

## Licence

GPL-3.0, as GOAD ([LICENSE](LICENSE)). This lab is deliberately vulnerable: keep it isolated.
