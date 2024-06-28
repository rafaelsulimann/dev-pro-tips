- Vamos agora **INSTALAR** e **CONFIGURAR** o **WILDFLY** no **ECLIPSE**.

# 1 - BAIXANDO O WILDFLY

- Para **BAIXAR** o **WILDFLY**, vamos **ACESSAR** o seguinte **SITE**:
- https://www.wildfly.org/downloads/
- Vamos então **BAIXAR** a **VERSÃO “MAIS ATUALIZADA”** do **“FINAL”** do **WILDFLY**.
- Depois vamos **DESCOMPACTAR** e **INSERIR** esta **PASTA** no **DISCO LOCAL “C”**.

# 2 - INSTALANDO O WILDFLY NO ECLIPSE

- Agora já no **ECLIPSE**, vamos **CONFIGURAR** o **WILDFLY** que já **BAIXAMOS** na nossa **IDE**.
- Para isso, vamos ir em **SERVERS → CREATE NEW SERVER.**

    <p>
        <img width="527" alt="1" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/5c22ff94-bcf7-4ffb-9ed5-0a9360a7e1b8">
    </p>

- Agora vamos **EXPANDIR** a **PASTA** do **“RED HAT JBOSS MIDDLEWARE”** e **SELECIONAR** a **“JBOSS AS, WILDFLY, & EAP SERVER TOOLS”**, e depois **CLICAR** em **“NEXT”**.

    <p>
        <img width="409" alt="2" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/4716a822-a5d4-43f3-abff-7b4053d7a974">
    </p>

- Então agora irá **COMEÇAR** a **REALIZAR** o **DOWNLOAD** de **VÁRIOS RECURSOS**.
- Depois de **INSTALADO** o **WILDFLY** e ter **RESTARTADO** o **ECLIPSE**, nós vamos **IR** em **SERVERS** novamente, e **CLICAR** em **“CREATE NEW SERVER”**.
- Perceba que agora nós **JÁ TEMOS** as **VERSÕES** do **WILDFLY** que estão **DISPONÍVEIS** para **UTILIZARMOS**, vamos **CLICAR** na **VERSÃO** mais atualizada.
    - **OBS:****** Caso a **VERSÃO DESEJADA “NÃO ESTEJA LISTADA”**, não se preocupe, pois **PODEMOS CONFIGURAR MANUALMENTE** depois a **VERSÃO** que **BAIXAMOS** lá do **SITE** do **WILDFLY**.

    <p>
        <img width="359" alt="3" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/7372d177-9f82-43b1-a063-b30e772ee64d">
    </p>

- Perceba que **NÃO TEM** a **VERSÃO 26** que é a que **IREMOS UTILIZAR**, porém mesmo assim, no **SERVER NAME** nós **IREMOS ALTERAR** para o **NOME** da **VERSÃO DESEJADA**.
- Depois **IREMOS** alterar novamente o nome no **RUNTIME**.
- E também, agora **IREMOS INSERIR** o **WILDFLY** que nós **BAIXAMOS** do **SITE**, para que desta forma ele **UTILIZE** da **VERSÃO DESEJADA**.
- Depois **IREMOS CONFIGURAR** para ele **UTILIZAR** a **VERSÃO** do **JDK** da forma **CORRETA**, caso ele **ESTEJA** com uma **VERSÃO** que **NÃO É** a **DESEJADA**.
- Ficará desta forma:

    <p>
        <img width="462" alt="4" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/198fab7b-036a-405a-a51d-15d6e164f613">
    </p>

- Depois disso, vamos dar um **FINISH**.

# 3 - ADICIONANDO COMANDO PARA NÃO APARECER ERRO AO STATRTAR O WILDFLY

- Agora vamos **ABRIR** o **eclipse.ini** e **INSERIR** o **SEGUINTE COMANDO** para **NÃO APARECER** este **ERRO**.

```
-startup
plugins/org.eclipse.equinox.launcher_1.6.400.v20210924-0641.jar
--launcher.library
plugins/org.eclipse.equinox.launcher.win32.win32.x86_64_1.2.500.v20220509-0833
-product
org.eclipse.epp.package.jee.product
-showsplash
org.eclipse.epp.package.common
--launcher.defaultAction
openFile
--launcher.defaultAction
openFile
--launcher.appendVmargs
-vm
C:/Program Files/Java/jdk-17.0.2/bin/javaw.exe
-vmargs
-Dosgi.requiredJavaVersion=11
-Dosgi.instance.area.default=@user.home/eclipse-workspace
-Dsun.java.command=Eclipse
-XX:+UseG1GC
-XX:+UseStringDeduplication
--add-modules=ALL-SYSTEM
-Dosgi.requiredJavaVersion=11
-Dosgi.dataAreaRequiresExplicitInit=true
-Dorg.eclipse.swt.graphics.Resource.reportNonDisposed=true
-Xms256m
-Xmx2048m
--add-modules=ALL-SYSTEM
**--add-opens=jdk.internal.jvmstat/sun.jvmstat.monitor=ALL-UNNAMED**
**--add-opens=java.base/java.security=ALL-UNNAMED**
```
