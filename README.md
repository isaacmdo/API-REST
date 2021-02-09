# API-REST
## Criação de uma API REST

<details>
  <summary>Configuração do ambiente</summary>
  
  
### Instalações necessárias local:
*Insomnia*, *MySql Workbench*

##### WINDOWS:
* 1 - bash: `choco install insomnia-rest-api-client`
* 2 - bash: `choco install mysql.workbench`
##### LINUX (UBUNTU)
* 1 - bash: `sudo apt install mysql-workbench`
* 2 - bash: `sudo snap install insomnia`


### Instalações necessárias servidor:

##### REMOVER VERSÕES ANTERIORES DO DOCKER
* 1 - bash: `sudo apt-get remove \`
      `docker \`
      `docker-engine \`
      `docker.io \`
      `containerd runc -y`
##### ATUALIZAR PACOTES    
* 2 - bash: `sudo apt update`
* 2.1 - bash: `sudo apt upgrade`

##### INSTALA O DOCKER-CE
* 3 - bash: `sudo apt install \`
      `apt-transport-https \`
      `ca-certificates \`
      `curl \`
      `gnupg-agent \`
      `software-properties-common -y`
* 3.1 - bash: `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`
* 3.2 - bash: `sudo add-apt-repository \`
              `"deb [arch=amd64] https://download.docker.com/linux/ubuntu \`
              `$(lsb_release -cs) \`
              `stable" -y`      
* 3.3 - bash: `sudo apt update`
* 3.4 - bash: `sudo apt install docker-ce docker-ce-cli containerd.io -y`

##### CRIANDO O CONTAINER DO MARIADB
* 4 - bash: `sudo docker run --restart always -d --name bdmariadb1 -p 3306:3306 \`
            `-e MYSQL_ROOT_PASSWORD=SUA_SENHA_FORTE mariadb`

##### COMANDOS DOCKER
*Para verificar o funcionamento do container:*
</br>

* bash: `sudo docker ps`

*Para parar o container criado:*
</br>

* bash: `sudo docker stop bdmariadb1`

*Para startar o container criado:*
</br>

* bash: `sudo docker start bdmariadb1`

*Para restartar o container criado:*
</br>

* bash: `sudo docker restart bdmariadb1`

*Para remover o container criado:*
</br>

* bash: `sudo docker rm bdmariadb1`

##### LIBERAR PORTA 3306
* 5 - Crie uma regra no firewall do servidor liberando o protocolo tcp na porta 3306 no seu servidor

##### CRIAR CONEXÃO
* 6 - Vá para o Mysql Workbench e cria uma conexão para o servidor na porta 3306

</details>

#### *LICENSE*
[![NPM](https://img.shields.io/npm/l/react)](https://github.com/zWeeeeelll/API-REST/blob/main/LICENSE) 

