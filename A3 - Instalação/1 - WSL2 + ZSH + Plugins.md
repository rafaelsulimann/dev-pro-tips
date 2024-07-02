# 1 - ABRA O POWERSHEEL DO WINDOWS E EXECUTE:

```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

# 2 - VERIFICAR REQUISITOS PARA EXECUTAR WSL2

- Para sistemas x64 (Windows): **Versão 1903** ou superiores, com o **Build 19042** ou superiores
- Para verificar:dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    - Tecla **Windows + R**
    - Digite: **winver**
- Para atualizar podemos ir no **iniciar - configurações do Windows update** e verificar atualizações para atualizar.

# 3 - HABILITAR O RECURSO MAQUINA VIRTUAL

```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

# 4 - REINICIAR COMPUTADOR

- Após **REALIZADA** os **COMANDOS ACIMA**, nós **PRECISAREMOS REINICIAR** o nosso **COMPUTADOR** para que ele **ATUALIZE** as **DEFINIÇÕES** no nosso **WINDOWS**.

# 5 - BAIXAR PACOTE DE ATUALIZAÇÃO DO KERNEL LINUX

https://dcomp.ufsj.edu.br/centro-de-recursos/tutoriais/93-wsl

- Clicar no link da **ETAPA 4** em **pacote de atualização kernel linux** para então baixar a atualização do linux.
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6e94f0b5-dae3-4632-8a03-6c1e0ce04c30/299be789-0b71-4778-b1e2-794090117227/Untitled.png)
- Após baixar, basta executar e instalar com as opções **default**.

# 6 - MUDAR VERSÃO PARA WSL2

- Abrir o **PowerShell** do Windows como **ADMINISTRADOR** e digitar:

```
wsl --set-default-version 2
```

# 7 - ADICIONAR O UBUNTO (VERSÃO MAIS RECENTE LTS) NO MICROSOFT STORE

- Abrir o menu iniciar e digitar: **microsoft store**
- Buscar na barra de pesquisa pelo nome **UBUNTU**
- Baixar a versão mais recente LTS do ubuntu.

# 8 - ABRIR O UBUNTU E CONFIGURAR

- Após abrirmos, ele automaticamente irá começar a instalar as configuração do ubuntu
- Inserir o **username** do **UNIX** que preferir
- Inserir a senha que preferir (obs:***não irá aparecer os caracteres na senha, mas os valores de fato estão sendo inserido caso voce esteja digitando algo)

# INSTALAÇÃO DO JAVA NO UBUNTU

- Após a instalação e configuração do ubuntu, para instalarmos o Java, podemos começar a digitar os comandos no Ubuntu:
    - **which java** = ele vai procurar para ver se tem alguma instalação do java
    - **which javac** = ele vai procurar se existe algum compilador do java

<aside>
👌🏻 OBS:***Se é a primeira vez que voce está instalando o ubunto, bem provavel que os comando acima irá dar erro, pois de fato nao vai haver nenhum programa do java ainda instalado

</aside>

- Caso tenha dado erro os comando acima, vamos então instalar o Java no Ubuntu.
- Digitando:

```
sudo apt install openjdk-11-jdk
```

- e depois falar que **sim** com a letra **Y**
- **sudo** = SuperUser, para conseguirmos baixar globalmente os programa com o usuario principal
**apt** = Gerenciador de pacote do Ubuntu
**install** = Comando para instalar
openjdk-11-jdk = **<nome do programa que queremos baixar>**
- Agora vamos dar o **UPDATE** dos pacotes para garantir que tudo será baixado e atualizado

```
sudo apt-get update
```

***DICA:***PODEMOS UTILIZAR A “SETA PARA CIMA” DO TECLADO PARA RETROSCEDER NO CONSOLE PARA OS COMANDO USADOS ANTERIORMENTE***

- Depois do **UPDATE** vamos fazer então o ***UPGRADE***.

```
sudo apt-get upgrade
```

- e depois falar que **sim** com a letra **Y**
- Depois iremos instalar o **Java**

```
sudo apt install openjdk-11-jdk
```

# OUTRAS CONFIGURAÇÕES

### 1 - ATIVAR OU DESTIVAR RECURSOS DO WINDOWS

- Precisamos aitvar algumas configurações também para ativar o linux no windows
- Primeiro vamos ir no menu **iniciar → painel de control → programas → ativar ou desativar recursos do windows**
- **habilitar** a opções:
    - **subsistema do Windows para Linux**
    - **plataforma de máquina virtual**

### 2 - BAIXAR A EXTENSÃO DO **REMOTE - WSL** NO **VSCODE**

- Para que possamos utilizar o WSL no Vscode, precisamos baixar a **extensao remote-wsl.**

### 3 - INSTALL ZSH

- Abrir o Ubuntu e digitar o comando para baixar o **ZSH**:

```
sudo apt install zsh
```

- Digitar o **username** e **senha** que ciramos do **UNIX**.

### 4 - TESTAR FUNCIONAMENTO

- Agora nós **VAMOS TESTAR** o **FUNCIONAMENTO** da **INSTALAÇÃO**.

```java
zsh --version
```

### 5 - INSTALAR OH-MY-ZSH

- Agora que **INSTALAMOS** o **ZSH**, nós **VAMOS INSTALAR** o **OH-MY-ZSH**.
- **OBSERVAÇÃO:***** para instalar nós **PRECISAREMOS** do **CURL** instalado.
- Então antes de **INSTALARMOS** o **OH-MY-ZSH** nós **VAMOS VERIFICAR** se nós **TEMOS** o **CURL INSTALADO**.

```java
curl --version
```

- Agora então nós **VAMOS INSTALAR** o **OH-MY-ZSH** a partir do seguinte **COMANDO**:

```java
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 6 - INSTALAR DRACULA THEME NO OH MY ZSH

- Para **INSTALARMOS** o **TEMA DRACULA** no **ZSH**, nós **VAMOS EXECUTAR** os **SEGUINTE COMANDOS:**

```java
git clone https://github.com/dracula/zsh.git
```

- Depois nós **PRECISAMOS COPIAR** o **ARQUIVO** chamado “dracula.zsh-theme” para o **DIRETÓRIO** de **TEMAS** do **OH MY ZSH**, conforme abaixo:

```java
Ubuntu-22.04\home\rafaelsulimann\.oh-my-zsh\themes
```

- Após isto, nós **PRECISAMOS ALTERAR** o **THEME** no **ARQUIVOS** do **“.ZSHRC”**.
- Para isso nós **VAMOS ENTRAR** neste **ARQUIVO** usando o **NANO**.

```java
sudo nano ./.zshrc
```

- Depois nós precisamos **ALTERAR** o **NOME** do **ZSH THEME** para **DRACULA**.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6e94f0b5-dae3-4632-8a03-6c1e0ce04c30/da6f4119-f5ac-489f-a5ae-a5d3bfc6fe84/Untitled.png)

- Para **SALVAR** as **ALTERAÇÕES**, nós **VAMOS APERTAR** o **“CTRL + X”**, dar um **YES**, depois **APERTAR DUAS VEZES** o **ENTER**.

### 7 - DEFINIR TEMA DRACULA NO WINDOWS TERMINAL

- Para **DEFINIRMOS** o **TEMA DRACULA** no **WINDOWS TERMINAL**, nós **PRECISAMOS**  do seguinte **JSON**:

```java
"schemes": [
    {
        "name": "Dracula",
        "cursorColor": "#F8F8F2",
        "selectionBackground": "#44475A",
        "background": "#282A36",
        "foreground": "#F8F8F2",
        "black": "#21222C",
        "blue": "#BD93F9",
        "cyan": "#8BE9FD",
        "green": "#50FA7B",
        "purple": "#FF79C6",
        "red": "#FF5555",
        "white": "#F8F8F2",
        "yellow": "#F1FA8C",
        "brightBlack": "#6272A4",
        "brightBlue": "#D6ACFF",
        "brightCyan": "#A4FFFF",
        "brightGreen": "#69FF94",
        "brightPurple": "#FF92DF",
        "brightRed": "#FF6E6E",
        "brightWhite": "#FFFFFF",
        "brightYellow": "#FFFFA5"
    }
]
```

- E depois **ALTERAR** o **PROFILE** da seguinte **FORMA**:

```java
"profiles": {
    "defaults": {
        "colorScheme" : "Dracula"
    }
}
```

### 8 - INSTALAR ZINIT PARA GERENCIAMENTO DE PLUGINS NO OH MY ZSH

- Agora nós **VAMOS INSTALAR** o **ZINIT** para nos **AUXILIAR** no **GERENCIAMENTO** dos **PLUGINS** que **VAMOS INSTALAR** no **OH MY ZSH**.
- Para isso, nós **VAMOS EXECUTAR** o seguinte **COMANDO**:

```java
bash -c "$(curl --fail --show-error --silent --location https://raw.githubusercontent.com/zdharma-continuum/zinit/HEAD/scripts/install.sh)"
```

### 9 - INSTALAR PLUGINS NO ZSH

- Agora nós **VAMOS INSTALAR** alguns **PLUGINS** no nosso **OH MY ZSH**, mas para isso, nós **PRECISAREMOS ENTRAR** no **ARQUIVO** do **.ZSHRC** e no **FINAL** do **ARQUIVO**, nós **VAMOS INSERIRS** as seguintes **LINHAS**:

```java
zinit light zdharma/fast-syntax-highlighting
zinit light zsh-users/zsh-autosuggestions
zinit light zsh-users/zsh-completions
```

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6e94f0b5-dae3-4632-8a03-6c1e0ce04c30/17687e38-9d11-4d2e-a1f4-1803bde8ce36/Untitled.png)
