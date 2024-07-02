- Agora nós **VAMOS APRENDER** um pouco **SOBRE** o **DOCKERFILE**.

# 1 - O QUE É DOCKERFILE?

- O **Dockerfile** é um **arquivo de texto** usado para **criar** uma **imagem Docker personalizada**. Ele **contém** uma **lista de instruções** que o **Docker** usa para **criar** uma **imagem**, com **base** em uma **imagem base**. A **imagem resultante** é um **pacote completo** que c**ontém tudo** o que é **necessário** para **executar** um **aplicativo**.
- O **Dockerfile** **pode ser dividido** em **duas partes principais**: a **primeira parte** é a **declaração da imagem base** e a **segunda parte** são as **instruções** que o **Docker** segue para **construir** a **imagem**.

## 1.1) PRIMEIRA PARTE

- Na **primeira parte** do **Dockerfile**, **especificamos** a **imagem base** a partir da qual queremos **construir** a nossa **imagem**. A **imagem base** é uma imagem existente que **contém todos os componentes necessários** para **executar** uma **aplicação específica**. Por exemplo, uma imagem base do Ubuntu pode ser usada para construir uma imagem personalizada com um aplicativo Node.js.

## 1.2) SEGUNDA PARTE

- Na **segunda parte** do Dockerfile, **listamos** as **instruções** que o **Docker** deve **seguir** para **construir** a **imagem personalizada.** **Cada instrução** do Dockerfile **cria** uma **camada** na **imagem resultante**. **Cada camada representa** um **conjunto de mudanças** que o **Docker fez** na **imagem base**. Essas **camadas** **podem** **ser reutilizadas** em o**utras imagens** e economizam espaço no armazenamento.

Abaixo estão alguns dos comandos mais comuns usados no Dockerfile:

- **FROM**: Especifica a imagem base a partir da qual a imagem personalizada será criada.
- **RUN**: Executa um comando durante a criação da imagem. Qualquer alteração feita durante a execução deste comando é salva como uma nova camada na imagem.
- **COPY**: Copia arquivos ou diretórios do host para a imagem. Esta instrução adiciona uma nova camada à imagem.
- **ADD**: Semelhante ao COPY, mas também suporta URLs e arquivos compactados.
- **WORKDIR**: Define o diretório de trabalho para a imagem.
- **EXPOSE**: Especifica as portas que a imagem expõe.
- **CMD**: Especifica o comando que será executado quando o contêiner for iniciado.
- **ENTRYPOINT**: Especifica o comando que será executado quando o contêiner for iniciado. É semelhante ao CMD, mas pode ser sobrescrito quando o contêiner é iniciado.

# 2 - CRIANDO O ARQUIVO “DOCKERFILE”

- Para que **POSSAMOS ESCREVER** os **COMANDOS** do **“DOCKER”** para **CRIAR** uma **IMAGEM**, nós **PRECISAMOS CRIAR** um **ARQUIVO DE TEXTO**, que **“DEVE”** se **CHAMAR** de **“Dockerfile”**.
- Devemos **RESPEITAR** as **“CAIXAS ALTAS E BAIXAS”** do **ARQUIVO DOCKERFILE**, ou seja, o **“D”** ele **DEVE SER “MAIÚSCULO”** e o **“RESTO MINÚSCULO”**.
- Nós **VAMOS CRIAR** este **ARQUIVO** na **PASTA PRINCIPAL** do **PROJETO**.

# 2 - EXEMPLO DE UM DOCKERFILE EM JAVA

- Aqui está um exemplo de como criar um Dockerfile para uma aplicação Java com Spring Boot:

```docker
# Imagem base
FROM openjdk:11

# Diretório de trabalho
WORKDIR /app

# Copia o arquivo JAR para a imagem
COPY target/myapp.jar /app

# Porta que será exposta
EXPOSE 8080

# Comando a ser executado
CMD ["java", "-jar", "myapp.jar"]

```

- Neste **exemplo**, **usamos** a **imagem** base do **OpenJDK 11** para **construir** a **nossa imagem**. Em seguida, **definimos** o **diretório de trabalho** como **/app** e **copiamos** o arquivo **JAR** da nossa **aplicação** para o **diretório de trabalho**. Em seguida, **usamos** a instrução **EXPOSE** para **expor** a **porta 8080**. Finalmente, **definimos** o **comando** que **será executado** quando o **contêiner** for **iniciado**.
