# jenkins_wsl

##Instalação no WSL
sudo apt update
sudo apt install openjdk-11-jre
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt update
sudo apt install jenkins


##Rodando junto com o docker
sudo docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts

##Obtendo a senha de administrador
sudo docker exec -it <nome_do_container_jenkins> cat /var/jenkins_home/secrets/initialAdminPassword
