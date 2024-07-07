# Execução de tarfas com Ansible

## Descrição:

Neste projeto, há a criação de duas máquinas virtuais **VM's**, usando a ferramenta Vagrant, no qual chamei-as de:

* Master e
* Node01

Onde a **Master** é máquina principal e nela sera instalado o **Ansible** e será provisionada pelo scirpt de shell chamado **provision-master.sh**

A máquina **Node01** será o agente ansible onde serao executadas as tarefas ordenadas pela máquina **Master**

Neste projeto contém as seguintes playbooks:

* create_user.ylm
Cria um usuário chamdo **Aldair** usando a variável `user_name`

* update_packs.yml
Atualiza os pacotes do sistema

* loop.yml
Instala uma lista de pacotes 

* webserver.yml
Instala o servidor web NGINX

* ubuntu-nodejs-server.yml
Instala e faz o deploy de uma aplicação node.js

## Como usar este projecto

Antes de iniciar, leia a página de documentação do Ansible para entender melhor a ferramenta e criar o seu iventario, poderá encontrá-la em [Ansible](https://docs.ansible.com/ansible/latest/getting_started/index.html)

Para criar as Maquinas, execute:

`vagrant up`

Para acessar as máquinas execute:

`vagrant ssh master` ou `vagrant ssh node_01`

Para destruir o ambiente execute:

`vagrant -f destroy`

Caso não tenha conhecimento das ferramentas usadas, encontrará a documentação em:

* [Vagrant](https://www.vagrantup.com/)
* [Virtualbox](https://www.virtualbox.org/)
