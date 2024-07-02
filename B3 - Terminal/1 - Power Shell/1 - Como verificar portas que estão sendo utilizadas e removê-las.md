- Agora nós **VAMOS APRENDER** como nós **VERIFICAMOS** as **PORTAS** que estão **SENDO UTILIZADAS** na nossa **MÁQUINA LOCAL** e também **COMO REMOVER** elas **MANUALMENTE** se necessário.

# 1 - VERIFICAR PORTA

- A **PRIMEIRA** coisa que **PRECISAMOS FAZER** é abrir o nosso **TERMINAL** e **VERIFICAR** se a **PORTA** específica **ESTÁ** sendo **UTILIZADA**.
- Para isso, basta **INSERIR** o seguinte **COMANDO:**

```
netstat -ano | findstr :<porta específica>
```

- Então desta forma nós **CONSEGUIMOS VERIFICAR** se **EXISTE** alguma **APLICAÇÃO** que **ESTÁ RODANDO** nesta **PORTA ESPECÍFICA.**

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a08f5e85-123e-4a0f-a091-03d37fbacaae/Untitled.png)

# 2 - REMOVER APLICAÇÃO MANUALMENTE

- Agora caso nós **QUISERMOS REMOVER** a **APLICAÇÃO** que **ESTÁ RODANDO** na **PORTA** específica, nós **PRECISAMOS “COPIAR”** o **NÚMERO “21008”** que **ESTÁ** no **FINAL** e **RODAR** o seguinte **COMANDO**:

```
taskkill /PID 21008 /F
```

- Então desta forma **IREMOS REMOVER** esta **APLICAÇÃO**.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/42eaa050-4889-4d13-8b12-605aa221e1d5/Untitled.png)
