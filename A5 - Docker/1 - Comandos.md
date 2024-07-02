# 1 - LISTAR OS CONTÂINERS

- Para nós **OBTERMOS/LISTARMOS** os **CONTÂINERS** que **ESTÃO “RODANDO”** atualmente na nossa **MÁQUINA LOCAL**, nós **VAMOS INSERIR** o seguinte **COMANDO** no **TERMINAL**:

```bash
docker ps
```

- Para **OBTERMOS/LISTARMOS** os **CONTÂINERS** que **ESTÃO “RODANDO”**, mas também os **CONTÂINERS** que em **ALGUM MOMENTO** nós **CRIAMOS** mas que **ATUALMENTE** ele **ESTÃO “PARADOS”**, nós **VAMOS INSERIR** o seguinte **COMANDO** no **TERMINAL**:

```bash
docker ps **-a**
```

- Nós também **TEMOS** outro **COMANDO**, que é o **“--size”**, pois neste caso, o **DOCKER** ele **VAI LISTAR** também os **CONTÂINERS** mas também **VAI INFORMAR** o **TAMANHO** do **CONTÂINER**.

```bash
docker ps **--size**
```

# 2 - LISTAR AS IMAGENS

- Para nós **OBTERMOS/LISTARMOS** as **IMAGENS** que **ESTÃO BAIXADAS** na nossa **MÁQUINA LOCAL**, nós **INSERIMOS** o seguinte **COMANDO**:

```bash
docker images
```

# 3 - REMOVER CONTÂINERS

- Para nós **REMOVERMOS** algum **CONTÂINER** nós **VAMOS INSERIR** o **COMANDO ABAIXO**:

```bash
docker rm <nome ou ID do container>
```

- Porém nós também **PODEMOS REMOVER**, **“FORÇANDO”** a **REMOÇÃO**, ou seja, mesmo que ele **ESTEJA EM EXECUÇÃO**, ele **SERÁ INTERROMPIDO E REMOVIDO**. Para isso, nós **VAMOS UTILIZAR** do **“-F”**. Ficará assim:

```bash
docker rm -f <nome ou ID do container>
```

# 4 - REMOVER IMAGENS

- Para **REMOVERMOS** alguma **IMAGEM** nós **VAMOS INSERIR** o seguinte **COMANDO**:

```bash
docker rmi <nome ou ID da imagem>
```

# 5 - BUILDAR UMA IMAGEM ATRAVÉS DE UM DOCKERFILE

- Para **CRIAR/BUILDAR** uma **IMAGEM** através de um **ARQUIVO “DOCKERFILE”**, nós **PRECISAMOS ENTRAR** nesta **PASTA** onde **DOCKERFILE** ele **ESTÁ SALVO** através do nosso **TERMINAL**, e depois **RODAR** o seguinte **COMANDO**:

```bash
docker build -t <nome da imagem>:<tag da imagem> .
```

# 6 - BAIXAR IMAGEM DO “DOCKER HUB”

- Para **BAIXAR** uma **IMAGEM** do **DOCKER HUB**, nós **INSERIMOS** o seguinte **COMANDO** no **TERMINAL**:
- **OBS:***** Se **NÃO FOR INFORMADA** a **TAG/VERSAO**, ele **IRÁ CONSIDERAR** a **ÚLTIMA VERSÃO**, no caso a **VERSÃO** com a **TAG “LATEST”**.

```bash
docker pull <image:tag/version>
```

# 7 - ENVIAR IMAGEM PARA O DOCKER HUB

- Para **ENVIARMOS** uma **IMAGEM LOCAL** para algum **REPOSITÓRIO** do **DOCKER HUB**, nós **VAMOS INSERIR** o seguinte **COMANDO** no terminal:

```bash
docker push <username/imagem:tag>
```

- Lembrando que para **ENVIARMOS** uma **IMAGEM** para algum **REPOSITÓRIO** do **DOCKER HUB**, nós **PRECISAMOS ESTAR “LOGADOS”** no nosso **DOCKER HUB** pelo **TERMINAL**.

# 8 - INSTANCIAR/INICIAR UM CONTAINER ATRAVÉS DE UMA IMAGEM

- Para nós **INSTANCIARMOS/INICIARMOS** um **CONTAINER LOCAL**, através de uma **IMAGEM** que **ESTÁ BAIXADA** no nosso **COMPUTADOR**, ou, **CASO NÃO ESTEJA**, ele **IRÁ BAIXAR** a **IMAGEM** lá do **DOCKER HUB**, caso ela **EXISTA**.
- Ficará assim:

```bash
docker run [OPTIONS] <image:tag> [COMMAND] [ARGS]
```

# 9 - STARTAR/STOPAR UM CONTÂINER

- Para nós **STARTARMOS** um **CONTÂINER EXISTENTE**, porém que atualmente ele **ESTÁ “STOPADO”**, nós **VAMOS INSERIR** o seguinte **COMANDO**:

```bash
docker start <nome ou ID do contâiner>
```

- Para **STOPAR** um **CONTÂINER** que atualmente **ESTÁ “EM EXECUÇÃO”**, nós **VAMOS INSERIR** o seguinte **COMANDO**:

```bash
docker stop <nome ou ID do contâiner>
```

# 10 - COMO SAIR DE UM CONTÂINER

- Para nós **SAIRMOS** de um **CONTÂINER**, quando **ESTIVERMOS “DENTRO” DELE**, nós **PODEMOS** **APERTAR** as seguinte **TECLAS**:

```bash
CTRL + (P -> Q)
```

- Ou nós **PODEMOS “INSERIR NO TERMINAL”**, o seguinte comando:

```bash
exit
```

- Porém, neste caso, nós **VAMOS SAIR**, mas também **VAMOS “STOPAR”** o **CONTÂINER**, já o **“CTRL + P→Q”** nós **SAÍMOS** mas **NÃO PARAMOS** o **CONTÂINER**.

# 11 - COMO ENTRAR EM UM CONTÂINER

- Para nós **ENTRAMOS** em um **CONTÂINER**, nós **VAMOS INSERIR** o seguinte **COMANDO** no **TERMINAL**:

```bash
docker attach <nome ou ID do contâiner>
```

- Porém, neste caso o **CONTÂINER** ele **PRECISA ESTAR “STARTADO”**.
- Nos caso em que nós **QUEREMOS “STARTAR”** e já **ENTRAR** dentro dele, nós **VAMOS INSERIR** o **“-ai”** no **COMANDO** que **JÁ MOSTRAMOS** do **“DOCKER START”**. Ficará assim:

```bash
docker start **-ai** <nome ou ID do contâiner>
```

# 12 - CONSULTANDO LOGS DE UM CONTÂINER

- Para nós **CONSULTARMOS** os **LOGS** do **CONTÂINER**, nós **VAMOS INSERIR** o seguinte **COMANDO**:

```bash
docker logs <nome ou ID do contâiner>
```

- Nós também **PODEMOS INSERIR** um **PARÂMETRO**, para que **ALÉM DE MOSTRAR** os **LOGS**, nós a partir daquele **MOMENTO**, nós **VAMOS ACOMPANHAR** os **LOGS** que **VIEREM** em **TEMPO REAL**, ou seja, nós **VAMOS ENTRAR** dentro do **CONTÂINER** para **VERIFICAR** os **LOGS**.
- Para isso, nós **VAMOS UTILIZAR** o **PARÂMETRO** do **“-f”**.
- Ficará assim:

```bash
docker logs **-f** <nome ou ID do contâiner>
```

# 13 - RELATÓRIO DE CONTÂINERS/IMAGENS DO DOCKER

- Nós **TEMOS** a **OPÇÃO** de **EMITIR** um **RELATÓRIO** com as **INFORMAÇÕES** sobre a **QUANTIDADE** de **CONTÂINERS** e **IMAGENS** e também o **TAMANHO DELAS**.
- Para isso, nós **VAMOS INSERIR** o seguinte **COMANDO**:

```bash
docker system df
```

# 14 - INPECIONAR INFORMAÇÕES DETALHADAS DA IMAGEM

- Para nós **INSPECIONARMOS** as **INFORMAÇÕES DETALHADAS** de uma **IMAGEM**, nós **VAMOS INSERIR** o seguinte **COMANDO** no terminal:

```bash
docker image inspect <nome ou ID da imagem>
```

# 15 - INPECIONAR INFORMAÇÕES DETALHADAS DO CONTÂINER

- Para nós **INPECIONARMOS** as **INFORMAÇÕES DETALHADAS** de um **CONTÂINER**, nós **VAMOS INSERIR** o seguinte **COMANDO** no terminal:

```bash
docker inspect <nome ou ID do contâiner>
```

# 16 - LISTAR TODOS OS VOLUMES LOCAIS

- Para **LISTAR** todos os **VOLUMES** que **EXISTEM** na nossa **MÁQUINA LOCAL**, nós **VAMOS INSERIR** o seguinte **COMANDO** no **TERMINAL**:

```bash
docker volume ls
```

# 17 - REMOVENDO VOLUME

- Para nós **REMOVERMOS** um **VOLUME** da nossa **MÁQUINA LOCAL**, nós **VAMOS INSERIR** o seguinte **COMANDO** no **TERMINAL**:

```bash
docker volume rm <id do volume>
```

- Ou nós **PODEMOS REMOVER** um **VOLUME** no **MESMO MOMENTO** que nós **REMOVEMOS** algum **CONTÂINER**, basta no **MOMENTO** de **REMOVER** o **CONTÂINER**, nós **INSERIMOS** o **PARÂMETRO** do **“-v”**.
- Ficará assim:

```bash
docker rm -v <nome ou id do contâiner>
```

# 18 - REALIZAR LOGIN NO DOCKER HUB PELO TERMINAL

- Para **REALIZAR** o **LOGIN** no **DOCKER HUB** pelo **TERMINAL** nós **VAMOS INSERIR** o seguinte **COMANDO**:

```bash
docker login docker.io
```

# 19 - LISTAR IMAGENS DE ALGUM USUÁRIO DO DOCKER HUB

- Para nós **LISTARMOS** as **IMAGENS** existentes de algum **USUÁRIO** específico do **DOCKER HUB**, basta nós **INSERIRMOS** o seguinte **COMANDO** no **TERMINAL**:

```bash
docker search <username>
```

# 20 - STARTAR/PARAR CONTÂINERS COM DOCKER-COMPOSE

- Quando **ESTIVERMOS UTILIZANDO** do **DOCKER-COMPOSE** para **SUBIR** os **CONTÂINERS** na **MESMA REDE**, nós **VAMOS UTILIZAR** o seguinte **COMANDO** para **SUBIR ELES**.
- **OBS:*****Lembrando que **PRECISAMOS INSERIR** este **COMANDO** no **MESMO DIRETÓRIO** de onde **SE ENCONTRAR** o **ARQUIVO** do **DOCKER-COMPOSE.YAML**.

```bash
docker-compose up -d
```

- Neste caso, nós **ESTAMOS UTILIZANDO** o **PARÂMETRO** do **“-d”**, para desta **FORMA** nós **INICIARMOS** os **CONTÂINER** de forma **“DETACHADA”**, ou seja, em **SEGUNDO PLANO**, sem **TRAVAR O TERMINAL**.
- E **QUANDO QUISERMOS “STOPAR”** esses **CONTÂINERS**, nós **VAMOS INSERIR** o seguinte **COMANDO**, também no **MESMO DIRETÓRIO**.

```bash
docker-compose down
```

# 21 - ENTRAR DENTRO DO CONTÂINER

- Caso nós **QUISERMOS ENTRAR** em algum **CONTÂINER ESPECÍFICO**, nós **PODEMOS INSERIR** o seguinte comando no **CONSOLE**:

```java
docker exec -ti <ID do contâiner> sh
```

- Desta forma, nós **VAMOS ENTRAR** dentro do nosso **CONTÂINER**, onde **PODEMOS VERIFICAR** os **DIRETÓRIOS** do **CONTÂINER**, e também **ADICIONAAR BIBLIOTECAS** com o **“APT-GET INSTALL”**.

# 22 - LIMPAR CACHE DO DOCKER

- Para limpar o cache do docker, vamos inserir o seguinte comando:

```jsx
docker builder prune
```

# 23 - MUDAR NOME/TAG DE UMA IMAGEM

- Para nós alterar o nome de uma imagem local, nós **VAMOS EXECUTAR** o seguinte comando:

```java
docker tag [IMAGE_ID_OR_NAME] [NEW_NAME]:[NEW_TAG]
docker tag meu-app:v1 meu-app:v2
```

- No caso, ao executar este comando, será criado uma noa imagem com o mesmo id, porém com tag diferente, mas a antiga imagem nao será deletada.
