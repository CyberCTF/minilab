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

Status: described and validated; not yet built end to end through Isoloom (GOAD and GOAD-Light
are).

## Licence

GPL-3.0, as GOAD ([LICENSE](LICENSE)). This lab is deliberately vulnerable: keep it isolated.
