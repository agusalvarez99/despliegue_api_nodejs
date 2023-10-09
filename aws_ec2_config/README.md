## Configurar Instancia EC2: Instalación de Git, Docker, Docker Compose, Node.js y NPM en Amazon Linux

### 1. Actualizar paquetes:
%%%bash
sudo yum update -y
%%%

### 2. Instalar Git:
%%%bash
sudo yum install git -y
%%%

### 3. Instalar Docker:
%%%bash
sudo yum install docker -y
sudo service docker start
sudo usermod -a -G docker ec2-user
%%%

### 4. Instalar Docker Compose:
%%%bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
%%%

### 5. Instalar Node.js y NPM:
%%%bash
curl --silent --location https://rpm.nodesource.com/setup_14.x | sudo bash -
sudo yum install -y nodejs
%%%
