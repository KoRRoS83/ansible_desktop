# Learning ansible automation 

## local.yml
This playbook is for building neovim from scratch and completing the initial configuration with nvim.kickstart.
```shell
korros@playbook-test:~/project/ansible_desktop$ ansible-playbook -K local.yml
SSH password: 
BECOME password[defaults to SSH password]: 
[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'

PLAY [Local playbook run for setting up Neovim] ********************************************************************************

TASK [Create config directory for nvim] ****************************************************************************************
ok: [localhost]

TASK [Install build prerequisites] *********************************************************************************************
ok: [localhost]

TASK [Git clone the neovim] ****************************************************************************************************
ok: [localhost]

TASK [Build neovim] ************************************************************************************************************
changed: [localhost]

TASK [Install neovim] **********************************************************************************************************
changed: [localhost]

TASK [Create config directory for nvim] ****************************************************************************************
ok: [localhost]

TASK [Add nodejs apt key] ******************************************************************************************************
ok: [localhost]

TASK [Add nodejs 19.x ppa for apt repo] ****************************************************************************************
ok: [localhost]

TASK [Install kickstart lsp requirements] **************************************************************************************
ok: [localhost]

TASK [Clone the neovim kickstart repo] *****************************************************************************************
ok: [localhost]

TASK [Copy kickstart.nvim init.lua to proper config directory] *****************************************************************
ok: [localhost]

PLAY RECAP *********************************************************************************************************************
localhost                  : ok=11   changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0 
```

## baseline.yml
This playbook is to make sure all servers are setup the same way, with the same base configuration.


Starting work on automationansible_desktop

