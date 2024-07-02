- Agora nós **VAMOS APRENDER** como nós **VERIFICAMOS** as **PORTAS** que estão **SENDO UTILIZADAS** na nossa **MÁQUINA LOCAL** e também **COMO REMOVER** elas **MANUALMENTE** se necessário.

# 1 - VERIFICAR PORTA

- A **PRIMEIRA** coisa que **PRECISAMOS FAZER** é abrir o nosso **TERMINAL** e **VERIFICAR** se a **PORTA** específica **ESTÁ** sendo **UTILIZADA**.
- Para isso, basta **INSERIR** o seguinte **COMANDO:**

```
netstat -ano | findstr :<porta específica>
```

- Então desta forma nós **CONSEGUIMOS VERIFICAR** se **EXISTE** alguma **APLICAÇÃO** que **ESTÁ RODANDO** nesta **PORTA ESPECÍFICA.**

  <p>
    <img width="440" alt="1" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/4232cb7f-4303-4c63-a996-05730be2b5fe">  
  </p>

# 2 - REMOVER APLICAÇÃO MANUALMENTE

- Agora caso nós **QUISERMOS REMOVER** a **APLICAÇÃO** que **ESTÁ RODANDO** na **PORTA** específica, nós **PRECISAMOS “COPIAR”** o **NÚMERO “21008”** que **ESTÁ** no **FINAL** e **RODAR** o seguinte **COMANDO**:

```
taskkill /PID 21008 /F
```

- Então desta forma **IREMOS REMOVER** esta **APLICAÇÃO**.

  <p>
    <img width="275" alt="2" src="https://github.com/rafaelsulimann/dev-pro-tips/assets/97992737/b88010a0-5d48-4dda-a042-82514c739db6">  
  </p>

