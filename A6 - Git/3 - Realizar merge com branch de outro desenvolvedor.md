- Agora nós **VAMOS APRENDER** a **COMO OBTER** as **ALTERAÇÕES** que **OUTRO DESENVOLVEDOR** ele **COMMITOU**, mas que ainda **NÃO REALIZOU** o **PULL REQUEST** para a **BRANCH PRINCIPAL**.
- Neste caso, como se **TRATA** de uma **BRANCH** de um **OUTRO DESENVOLVEDOR** que já **ESTÁ** no **REPOSITÓRIO REMOTO**, nós **PRECISAMOS OBTER** esta **BRANCH** no nosso **REPOSITÓRIO LOCAL**, pois nós **AINDA NÃO TEMOS** ela.

# 1 - FAZER BACKUP DAS NOSSAS ALTERAÇÕES

- A **PRIMEIRA** coisa que **PRECISAMOS FAZER** é o **BACKUP** das nossa **ALTERAÇÕES ATUAIS** da **NOSSA BRANCH**, pois **PRECISAREMOS VOLTAR** para a **BRANCH PRINCIPAL** para **ATUALIZAR** o  **ESTADO ATUAL** da **BRANCH PRINCIPAL** com as **NOVAS ALTERAÇÕES**.
- Para isso, nós **VAMOS EXECUTAR** o seguinte **COMANDO** na nossa **BRANCH** da **FEATURE**:

```bash
git stash push -m "<mensagem do stash>"
```

- Após isto, nós **PODEMOS VOLTAR** para a **BRANCH PRINCIPAL** através do seguinte **COMANDO**:

```bash
git checkout <nome da branch principal>
```

# 2 - ATUALIZAR REPOSITÓRIO LOCAL EM RELAÇÃO AO REMOTO

- Agora nós **PRECISAMOS ATUALIZAR** o nosso **REPOSITÓRIO LOCAL** em **RELAÇÃO** ao **REPOSITÓRIO REMOTO** para que **POSSAMOS OBTER** as **NOVAS BRANCHS** e também o **COMMITS**.
- Para isso, nós **VAMOS EXECUTAR** o seguinte **COMANDO**:

```bash
git fetch origin
```

- Neste caso nós **USAMOS** o **FETCH** pois ele **APENAS ATUALIZA** os **COMMITS/BRANCHS** mas **NÃO ATUALIZA** o **CÓDIGO** de fato.
- Agora **PARA VISUALIZARMOS** se o nosso **REPOSITÓRIO LOCAL** ele já **INCLUIU** o **REPOSITÓRIO** do **OUTRO DESENVOLVEDOR**, nós **PODEMOS EXECUTAR** o seguinte **COMANDO**:

```bash
git branch -r
```

- Neste caso, como nós **ESTAMOS INSERINDO** o **PARÂMETRO** do **“-r”** que **SIGNIFICA “REMOTE”**.
- Então ele **VAI LISTAR** apenas as **BRANCHS** do nosso **REMOTE**, algo que **NÃO ACONTECERIA** se nós **NÃO TIVÉSSEMOS INSERIDO** o **PARÂMETRO**, pois neste caso ele **LISTARIAS** apenas as **BRANCHS** do nosso **REPOSITÓRIO LOCAL**, que **AINDA NÃO POSSUI** a **BRANCH** do **OUTRO DESENVOLVEDOR**.

# 3 - CRIAR BRANCH LOCAL ATRAVÉS DA BRANCH DO OUTRO DESENVOLVEDOR

- Agora nós **PRECISAREMOS CRIAR** uma **BRANCH LOCAL** através da **BRANCH** do **OUTRO DESENVOLVEDOR** que **OBTIVEMOS** através do **COMANDO** do **“git fetch origin”**.
- Pois atualmente nós **OBTIVEMOS** apenas a **BRANCH** do **REMOTE**, mas **NA PRÁTICA** nós **AINDA NÃO TEMOS** esta **BRANCH** no nosso **REPOSITÓRIO LOCAL**, então para isso, nós **PRECISAMOS CRIAR** uma **BRANCH** que **REPLICA** a **CÓDIGO** da **BRANCH** do **REMOTE**.
- Para isso, nós **PRECISAREMOS EXECUTAR** o seguinte **COMANDO** para **CRIAR** esta **NOVA BRANCH LOCAL** a partir da **BRANCH** do **REMOTE**.

```bash
git checkout -b <nome da nova branch local> <nome da branch do remote que desejamos replicar>
#git checkout -b MM_FEATURE_DTFSCBCRED10942 origin/MM_FEATURE_DTFSCBCRED10942
```

# 3 - ALTERAR PARA A NOSSA FEATURE BRANCH

- Agora que **CRIAMOS** uma **BRANCH LOCAL** que **É** a **RÉPLICA** da **BRANCH** do **OUTRO DESENVOLVEDOR** do **REMOTE**, nós **VAMOS VOLTAR** para a nossa **FEATURE BRANCH** que **ESTÁVAMOS REALIZANDO** a nossa **IMPLEMENTAÇÃO**, através do seguinte **COMANDO**:

```bash
git checkout <nome da nossa feature branch>
```

# 4 - REALIZAR MERGE OU REBASE DA NOSSA FEATURE BRANCH COM A BRANCH LOCAL RÉPLICA DO OUTRO DESENVOLVEDOR

- Agora que **ESTAMOS** na nossa **FEATURE BRANCH**, nós **PRECISAMOS REALIZAR** o **MERGE** ou o **REBASE** com a **BRANCH LOCAL** que **É** a **RÉPLICA** da **BRANCH** do **OUTRO DESENVOLVEDOR**.
- **FAZENDO ISSO**, nós **ESTAMOS OBTENDO** todas as **ALTERAÇÕES** que a **BRANCH RÉPLICA** tem de **DIFERENTE** em **RELAÇÃO** a nossa **FEATURE BRANCH**.
- Mas **QUANDO USAR** o **MERGE** ou **REBASE**?
- Os **DOIS CASOS** eles **VAI REALIZAR** a **REPLICAÇÃO** das **ALTERAÇÕES** para a nossa **FEATURE BRANCH**, porém o **MERGE** ele **GERA** um **COMMIT ADICIONAL** para **INFORMAR** que **FOI FEITO** a **REPLICAÇÃO** com a **BRANCH** do **OUTRO DESENVOLVEDOR**, e no caso do **REBASE** ele apenas **VAI FAZER** a **REPLICAÇÃO** mas **NÃO VAI GERAR** este **COMMIT ADICIONAL**.
- Para isso, **PRECISAREMOS EXECUTAR** o seguinte **COMANDO**:

```bash
git rebase <nome da branch local que é replicado da branch do outro desenvolvedor>
#ou
git merge <nome da branch local que é replicado da branch do outro desenvolvedor>
```

# 5 - RETORNAR AS NOSSAS ALTERAÇÕES QUE ESTAVA NO BACKUP

- Agora que nós **REALIZAMOS** a **REPLICAÇÃO** da **BRANCH** do **OUTRO DESENVOLVEDOR** para a nossa **FEATURE BRANCH**, nós **PRECISAMOS RETORNAR** as nossas **ALTERAÇÕES** que **ESTÃO** no **BACKUP**.
- Para isso, nós **VAMOS EXECUTAR** o seguinte **COMANDO**:

```bash
git stash pop
```

- Desta forma, nós **ESTAMOS TRAZENDO** do **BACKUP** o **ÚLTIMO “STASH” REALIZADO**.
- Lembrando que **ESTE COMANDO** ele **PODE GERAR “CONFLITO”** entre as **BRANCHS**, na qual nós **PRECISAREMOS RESOLVER** os **CONFLITOS** caso ocorram.
