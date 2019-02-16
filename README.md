
# Usage

1. Enter target ips into the inventory file
2. Edit defaults/main.yml as you wish
3. Check out the warnings
4. Run

```bash
ansible-playbook -i inventory role.yml
```


# What this role can do for you?
*This role will install all the required software for a PostgreSQL9.4 BDR
*  This role will add the required bdr parameters to the postgresql.conf
* This role will add a trust rule for every node in the inventory file
* This role will start the bdr from the initial node and join all the other nodes to bdr

[PostgreSQL BDR website](https://www.2ndquadrant.com/)
[BDR 1 Documentation](http://bdr-project.org/docs/1.0.3/index.html)

# Warnings
* This script is made for Centos/Redhat based distros, (debian support will be added on next release)
* Make sure nodes can connect to each other. Configure or firewalld and iptables before running the role    
* Set hostnames on nodes and makes sure the hostnames are unique , these names will be used as node names when joining to the BDR.
* pg_hba trust rule for every ip will be added, so be ware.
