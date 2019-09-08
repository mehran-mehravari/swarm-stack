##Prerequisites

1. Running a swarm cluster including 3 manager and 3 worker nodes

* Tag manager nodes in order to make sure elastisearch master nodes are installed on each swarm manager node  
  - docker node update --label-add elk=master NODE-ID
    note: replace appropriate name to NODE-ID through "docker node ls" command

2. Setup Infrastructure

* Tune kernel parameters as follows:
  - vm.swappiness=1
  - net.core.somaxconn=65535
  - vm.max_map_count=262144
  - fs.file-max=518144

* add the item below to docker.service
  - LimitMEMLOCK=infinity

* To effect the changes
  - docker-daemon reload
  - systemctl restart docker
