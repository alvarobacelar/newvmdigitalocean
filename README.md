NEWVMDIGITALOCEAN
=========

Essa role tem como objetivo criar novos droplets na digitalocean.

Requisitos
------------

Para executar essa role com sucesso, é preciso ter a api da digitalocean em /home/.apidigitalocean para poder conseguir criar a vm.

Role Variaveis
--------------

Para a execução com sucesso dessa role é preciso passar algumas variáveis no playbook da execução, conforme o exemplo abaixo

Example Playbook
----------------

Exemplo de playbook de execução dessa role:
i
    - hosts: localhost
      connection: local
      vars:
    	estado: present
    	ram: 2gb
    	ram_master: 2gb
    	droplet_name_master: master01
    	droplet_worker:
          - node01
          - node02
    	tag_name: cluste01
    	master: yes
    	droplet_grupo: cluster01
      	gather_facts: false
      roles: 
    	- newvmdigitalocean
      

