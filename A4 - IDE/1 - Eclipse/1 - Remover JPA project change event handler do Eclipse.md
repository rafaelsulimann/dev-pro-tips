- Agora nós **VAMOS APRENDER** sobre **COMO REMOVER** a **VALIDAÇÃO** do **JPA PROJECT CHANGE EVENT HANDLER** do **ECLIPSE**.

# 1 - REMOVER TODAS VALIDAÇÕES NA SESSÃO DE “PREFERENCES” DO ECLIPSE

- A **PRIMEIRA** coisa que **PRECISAREMOS FAZER** será **REMOVER** todas as **VALIDAÇÕES** do **ECLIPSE** na **ABA** de **“PREFERENCES”** do **ECLIPSE**.
- Para isso nós **VAMOS ABRIR** esta **SESSÃO** de **PREFERENCES** seguindo o seguinte **CAMINHO** nas **ABAS**:
    - Windows → Preferences
    
    <p style="margin-top: 20px;">
      <img padding="10" width="184" alt="1" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/4f5da08d-f3dd-477c-9189-5cba0bac689f">
    </p>


- Agora com esta **JANELA** de **PREFERÊNCIAS ABERTA**, nós **VAMOS ENTRAR** em **“VALIDATION”**, conforme imagem abaixo:

    <p>
        <img width="122" alt="2" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/97fbbcaf-3c53-4976-a89d-3c61a64953f7">
    </p>

- Agora nós **VAMOS “DESABILITAR”** todas as **VALIDAÇÕES** desta **PÁGINA**, e para isso, nós **VAMOS “DESMARCAR”** a **OPÇÃO** de **“SUSPEND ALL VALIDATOR”**, ou apenas **CLICAR** em **“DISABLE ALL”**, conforme abaixo:

    <p>
        <img width="531" alt="3" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/c4b1305c-310e-48aa-b73f-b7c3eba65dce">
    </p>

# 2 - REMOVER LINHA DO JPA NO ARQUIVO DE CONFIGURAÇÃO DO ECLIPSE

- Agora nós **PRECISAREMOS REMOVER** as **LINHAS** do **JPA** que estão no **ARQUIVO DE CONFIGURAÇÃO** do **ECLIPSE**, para que **DESTA FORMA**, o **ECLIPSE** realmente **NÃO REALIZE** mais **NENHUMA VALIDAÇÃO** no momento do **DESENVOLVIMENTO**.
- Para isso, nós **PRECISAREMOS ENCONTRAR** o **LOCAL** onde a **PASTA** do **ECLIPSE** está **SALVA**, então nós **PODEMOS** apenas **CLICAR** com o **BOTÃO DIREITO** em **CIMA** do **EXECUTÁVEL** do **ECLIPSE** que nós **UTILIZAMOS** e **CLICAR** em **“ABRIR LOCAL DO ARQUIVO”**, conforme abaixo:

    <p>
        <img width="532" alt="4" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/5161880a-3f43-41d1-b599-32dd2722aaba">
    </p>

- Agora então nós **VAMOS ACESSAR** o seguinte **CAMINHO**:
    - Configuration/org.eclipse.equinox.simpleconfigurator
- Após isto, nós **VAMOS ENTRAR** na seguinte **PASTA** que **POSSUI** o **ARQUIVO** do **“BUNDLES.INFO”.**

    <p>
        <img width="533" alt="5" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/cdb58607-4ef1-4da0-9f1e-8c64dee9d9a3">
    </p>

- Agora nós **PRECISAREMOS ABRIR** este **ARQUIVO** como **ADMINISTRADOR**, **USANDO** o **“NOTEPAD++”**.
- Após isto, nós **PRECISAREMOS DELETAR** todas as **LINHAS** que **COMEÇAM** com **“ORG”** e **POSSUAM** o nome **JPA** em **ALGUMA PARTE** do nome.
- Então a partir de agora, após **DELETAR** e **SALVAR**, o **ECLIPSE** ele **NÃO REALIZARÁ** nenhuma **VALIDAÇÃO** após alguma **ALTERAÇÃO** do **CÓDIGO** em **DESENVOLVIMENTO**.
