- Agora nós **VAMOS APRENDER** a como **INSTALAR** o **DOCKER ENGINE** no **WSL2**.

# 1 - INSTALAR DEPENDÊNCIAS

- A **PRIMEIRA COISA** que **PRECISAMOS FAZER** será **INSTALAR** algumas **DEPENDÊNCIAS** do **DOCKER ENGINE**, conforme **COMANDOS** abaixo:

```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

# Add the repository to Apt sources:
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

# 2 - INSTALAR DOCKER

- Agora nós **VAMOS INSERIR** o **COMANDO** para **INSTALAR** o **DOCKER ENGINE**.

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

# 3 - ATIVA O DOCKER ENGINE

- Agora nós **PRECISAMOS STARTAR** o **DOCKER ENGINE**, através do seguinte comando:

```bash
sudo service docker start
```

# 4 - ADICIONAR PERMISSÕES

- Agora nós **VAMOS ADICIONAR** algumas **PERMISSÕES** para **CONSEGUIRMOS UTILIZAR** o **DOCKER**, conforme **COMANDOS** abaixo:

```bash
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

# 5 - TESTAR FUNCIONAMENTO

- Agora nós **VAMOS TESTAR** o **FUNCIONAMENTO** dando um **COMANDO** do **“DOCKER PS”**.

  <p>
    <img width="479" alt="1" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/d4904461-8e92-451f-83c3-403ef633bb4f">  
  </p>

- Então **DEU TUDO CERTO!**

# 6 - INSTALAR DOCKER-COMPOSE

- Agora nós **VAMOS INSTALAR** o **DOCKER COMPOSE** no nosso **WSL2**, pois ele **NÃO VEM INSTALADO** por **DEFAULT** quando **INSTALAMOS** o **DOCKER ENGINE**.
- A **PRIMEIRA** coisa que **PRECISAREMOS FAZER** será **ACESSAR** o **GITHUB** do **DOCKER COMPOSE** para **VERIFICAR** a **VERSÃO** mais **RECENTE** do **DOCKER COMPOSE**, para isso, nós **VAMOS ACESSAR** o seguinte site:

[Releases · docker/compose](https://github.com/docker/compose/releases)

- Agora que **SABEMOS** a **ÚLTIMAS VERSÃO**, nós **VAMOS EXECUTAR** o seguinte **COMANDO** no **TERMINAL WSL2**:

```python
sudo curl -L "https://github.com/docker/compose/releases/download/{ULTIMA_VERSAO}/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

- Agora nós **VAMOS EXECUTAR** o seguinte **COMANDO** para **DEIXAR** o **BINÁRIO** do **DOCKER COMPOSE “EXECUTÁVEL”**:

```python
sudo chmod +x /usr/local/bin/docker-compose
```

- Agora nós **PRECISAREMOS INSERIR** a seguinte **VARIÁVEL DE AMBIENTE** no nosso **ZSHRC**:

```python
export PATH=$PATH:/usr/local/bin
```

- Feito isso, nós **PODEMOS EXECUTAR** o **COMANDO ABAIXO** para **EXECUTAR** a **ATUALIZAÇÃO** no **ZSHRC**:

```python
source ~/.zshrc
```

- Então agora nós **PODEMOS EXECUTAR** o seguinte **COMANDO** para **VERIFICAR** se **DEU CERTO**:

```python
docker-compose --version
```
