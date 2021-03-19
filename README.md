# THIS REPO IS NO LONGER MAINTAINED
# FOR OCTOPUS OR HIGHER SUPPORT SEE HERE INSTEAD https://github.com/45Drives/ceph-ansible
# ceph-ansible-45d

- Chassis supported:
  - HDD/Hybrid (AV15,Q30,S45,XL60 - H16,H32)
- Install from rpm or git clone to '/usr/share/ceph-ansible'
- Create Inventory file 'hosts'
  - Required groups:
    - mons
    - mgrs
    - osds
  - see hosts.sample for all options
- Fill out group_vars/all.yml
  - monitor_interface
  - public_network
  - cluster_network
  - hybrid_cluster
- Generate device alias
  - ansible-playbook -i hosts device-alias.yml
- Generate osd vars
  - ansible-playbook -i hosts generate-osd-vars.yml
- Deploy cluster
  - ansible-playbook -i hosts core2.yml
