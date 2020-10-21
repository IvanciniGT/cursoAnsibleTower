# cursoAnsibleTower

## Tareas para instalación.

### Ansible <<---
sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install ansible -y
ansible --version
### Ansible Tower AWX <---
    Docker                  sudo apt install docker
    Docker-compose          sudo apt install docker-compose
                            sudo pip3 install docker
                            sudo pip3 install docker-compose
    NodeJs (interprete de javascript)
                            sudo apt install nodejs
    NPM Gestor de paquetes para JS
                            sudo apt install npm
                            sudo npm install npm --global
    


Ansible: 
    ansible_facts: 
        custom_facts <--- modulo: set_fact
                          meter un fichero JSON dentro de la carpeta /etc/ansible/facts
                          
Organización: Automatización
    Inventarios:
        PRE
            Grupos:
                jenkins
                basededatos
                    ---> Ubuntu
                    ---> Windows
                    ---> Redhat
                webserver
                    ---> CentOS
                    ---> Windows
        Pro
            Grupos:
                jenkins
                basededatos
                webserver
                    ---> Redhat
                    ---> Windows

Proceso (playbook) de actualización de la versión de UBUNTU
    Inventario inteligente: 
        Ubuntu:
            PRE-basededatos- bdpre1.db            
            PRO-basededatos- bdpro2.db            
            PRO-webserver  - webserver1.web