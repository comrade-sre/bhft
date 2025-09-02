test playbook && role for bhft 
============================
Features 
-------
* Wokrs on ubuntu 
* Allows to create partitions and encrypt them 
* Rename network interface 
* Print cpu info 

Role Variables 
* `packages` 
    list of packages you need to 
* `device_for_partition` 
    device on which partition will be created 
* `fs_type` 
     filesystem for the new partition 
* `keyfile_path` 
    path to key for luks encryption 
* `to_encrypt` 
    list of partition to encrypt, check partition's size before encryption   
Instruction:  
Make sure you have a private key for access to target host in path $HOME/.ssh/aws-test-user  
Check the variables for the target group:  
`group_vars/test/vars.yml`  
Run the playbook in check mode without tags:  
`ansible-playbook main.yaml -CDv`  
List of possible tags:  
`ansible-playbook main.yml --list-tags`  

