# HA-Pipeline



## Step 1: Ensure Ansible plugin is installed 
## Step 2: Add Ansible controller as a slave under the group "ansiblecontroller" & copy the public key of master to authorized-key on controller 
## Step 3: Add a secret of text type for ansible vault with the name "ansiblevault"
## Step 4: Add 1 more controller & try HA 
