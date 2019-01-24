# FIRST PLAYBOOKS...

* ssh user@doublewopr.mux.isinfra.net using you TACACS account
* git clone https://github.com/h3phaistos/Ansible4rookies.git

* ## 1-show_vlans.yaml:
	* GOAL: 'show' command on Cisco router and display the output
	* LAUNCHING:  ansible-playbook 1-show_vlans.yaml -u <USER_ID> -k

* ## 2-show_vlan_id_fail.yaml:
	* GOAL: Ansible tasks can generate playbook failure due to device output returned.
	* LAUNCHING:  ansible-playbook 2-show_vlan_id_fail.yaml -u <USER_ID> -k -e vlan=<VLAN_ID>

* ## 3-show_vlan_id_success.yaml:
	* GOAL: explicitly tell ansible when a task must be considered failed
	* LAUNCHING:  ansible-playbook 3-show_vlan_id_success.yaml -u <USER_ID> -k -e vlan=10

* ## 4-config_vlan.yaml:
	* GOAL: Configure VLAN after executing a few checks
	* LAUNCHING:  ansible-playbook 4-config_vlan.yaml -u <USER_ID> -k -e vlan=10 --diff
	* LAUNCHING:  ansible-playbook 4-config_vlan.yaml -u <USER_ID> -k -e vlan=101 --diff
