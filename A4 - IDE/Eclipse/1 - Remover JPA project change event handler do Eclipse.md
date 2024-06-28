- Agora nós **VAMOS APRENDER** sobre **COMO REMOVER** a **VALIDAÇÃO** do **JPA PROJECT CHANGE EVENT HANDLER** do **ECLIPSE**.

# 1 - REMOVER TODAS VALIDAÇÕES NA SESSÃO DE “PREFERENCES” DO ECLIPSE

- A **PRIMEIRA** coisa que **PRECISAREMOS FAZER** será **REMOVER** todas as **VALIDAÇÕES** do **ECLIPSE** na **ABA** de **“PREFERENCES”** do **ECLIPSE**.
- Para isso nós **VAMOS ABRIR** esta **SESSÃO** de **PREFERENCES** seguindo o seguinte **CAMINHO** nas **ABAS**:
    - Windows → Preferences

    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6e94f0b5-dae3-4632-8a03-6c1e0ce04c30/fa326819-9cb1-4abf-aff8-b7825d76de45/Untitled.png)

- Agora com esta **JANELA** de **PREFERÊNCIAS ABERTA**, nós **VAMOS ENTRAR** em **“VALIDATION”**, conforme imagem abaixo:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6e94f0b5-dae3-4632-8a03-6c1e0ce04c30/17e15402-0b8f-4c1d-afd4-e5aca69e4bf9/Untitled.png)

- Agora nós **VAMOS “DESABILITAR”** todas as **VALIDAÇÕES** desta **PÁGINA**, e para isso, nós **VAMOS “DESMARCAR”** a **OPÇÃO** de **“SUSPEND ALL VALIDATOR”**, ou apenas **CLICAR** em **“DISABLE ALL”**, conforme abaixo:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6e94f0b5-dae3-4632-8a03-6c1e0ce04c30/b6f726e7-5b29-49cb-92a2-b8ffe765c99f/Untitled.png)

# 2 - REMOVER LINHA DO JPA NO ARQUIVO DE CONFIGURAÇÃO DO ECLIPSE

- Agora nós **PRECISAREMOS REMOVER** as **LINHAS** do **JPA** que estão no **ARQUIVO DE CONFIGURAÇÃO** do **ECLIPSE**, para que **DESTA FORMA**, o **ECLIPSE** realmente **NÃO REALIZE** mais **NENHUMA VALIDAÇÃO** no momento do **DESENVOLVIMENTO**.
- Para isso, nós **PRECISAREMOS ENCONTRAR** o **LOCAL** onde a **PASTA** do **ECLIPSE** está **SALVA**, então nós **PODEMOS** apenas **CLICAR** com o **BOTÃO DIREITO** em **CIMA** do **EXECUTÁVEL** do **ECLIPSE** que nós **UTILIZAMOS** e **CLICAR** em **“ABRIR LOCAL DO ARQUIVO”**, conforme abaixo:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6e94f0b5-dae3-4632-8a03-6c1e0ce04c30/e6074054-edc4-4fc4-a38f-2742cd2b07b9/Untitled.png)

- Agora então nós **VAMOS ACESSAR** o seguinte **CAMINHO**:
    - Configuration/org.eclipse.equinox.simpleconfigurator
- Após isto, nós **VAMOS ENTRAR** na seguinte **PASTA** que **POSSUI** o **ARQUIVO** do **“BUNDLES.INFO”.**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6e94f0b5-dae3-4632-8a03-6c1e0ce04c30/c24c4541-006f-4342-ad51-4bbaeca3012a/Untitled.png)

- Agora nós **PRECISAREMOS ABRIR** este **ARQUIVO** como **ADMINISTRADOR**, **USANDO** o **“NOTEPAD++”**.
- Após isto, nós **PRECISAREMOS DELETAR** todas as **LINHAS** que **COMEÇAM** com **“ORG”** e **POSSUAM** o nome **JPA** em **ALGUMA PARTE** do nome.
- Então a partir de agora, após **DELETAR** e **SALVAR**, o **ECLIPSE** ele **NÃO REALIZARÁ** nenhuma **VALIDAÇÃO** após alguma **ALTERAÇÃO** do **CÓDIGO** em **DESENVOLVIMENTO**.
