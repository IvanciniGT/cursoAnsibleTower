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
            

Instalación de Ansible TOWER / AWX
Playbook -> 4 contenedores -> docker-compose 
    - Web
    - Task
    - Postgresql
    - redis

GUAY !!! -> AUTOMATIZADO (ansible)
    Esta instalación me sirve para un entorno de PRO ?
        Alta disponibilidad <- UNA UNICA MAQUINA 
            -> CLUSTER

Kubernetes <- Orquestar contenedores en un cluster
   VV
   VV
  Redhat  <- Openshift
  
  
 Cluster:
 
    Nodos:
        Nodo1
            Postgresql <- 1 contenedor 
                Escalabilidad: con 1 sobra...
                HA?:           Igual, me sobra... Kubernetes... Openshift (Volumenes)
        Nodo2
            Redis??? <- Carga de trabajo poca
                Escalabilidad: 1 sobra
                HA?:           2 
        Nodo3
            Web??? <- 100 personas concurrentes
        Nodo4
            Task <--- ??? Ni idea... depende... peero este es el que curra
        Nodo5
        ...
        Nodo 10
        
         
Red interna 1
    Host 1
    Host 2
    Host 3
Red interna 2
    Host A 
    Host B
DMZ 
    Host a
    Host b
    Host c


Ansible Tower -> Mogollon de contenedores.... Contenedores de tipo TASK
                                                VVVV
                                              Kubernetes / Openshift
                                                    Algunos nodos conectados a Red interna 1
                                                        task C1---- TASK_INTERNOS_1
                                                        task C2----
                                                    Otros nodos conectados a red internat 2
                                                        task C11---- TASK_INTERNOS_2
                                                        task C21----
                                                    Mas nodos conectados a la DMZ
                                                        task C22---- TASK_DMZ 
                                                        task C23----




Carlos Martinez
--------------- 
Gestión de configuración
Comprobaciones de entornos remotos

Servidores de aplicaciones:
    JBoss
    IIS

    - Linux
        RedHat
        Ubuntu
    - Windows
    

    Instalar
        ---> Librerias
        ---> Servidor de Apps
    Upgrades
        ---> Librerias
        ---> Servidor de Apps
    Despliegues
        ---> Apps
    Reinicios
        ---> Servidores de apps
        ---> Apps
        ------------------
    Ampliar FS
        ---> SO + Cada App
        ---> Otros
    
    Instalación en un WAP ---> HA ----> Cluster (4)
        Instalación de una maquina 5

        Maquina 5 sea accesible por mis clientes: Frontal (Balanceador de carga...)
            ---> Reconfigurar Frontal servidor


    
    

