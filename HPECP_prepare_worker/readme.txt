=================================================================
How to prepare K8s worker hosts to install HPE Container Platform
=================================================================

1. Install ansible ver >= 2.7 to management host (maybe hpecp controller)
	# yum install -y ansible
2. Copy files from HPECP_prepare_worker to ansible host 
	for example to:  ~/ansible/hpecp-prepare-worker
3. Change directory	
    # cd ~/ansible/hpecp-prepare-worker
4. Add K8s worker hosts to [k8s_workers] section of hosts file
    # vi hosts
5. Run ansible playbook prepare-worker.yml
	# ansible-playbook --ask-pass prepare-worker.yml
   
    