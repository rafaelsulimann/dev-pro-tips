- Agora nós **VAMOS APRENDER** o **PROCESSO** que **SEMPRE DEVEMOS FAZER** antes de **COMMITAR** as **ALTERAÇÕES** da nossa **FEATURE BRANCH**.
- Basicamente sempre **ANTES** de **COMMITAR**, nós **DEVEMOS ATUALIZAR** a **BRANCH PRINCIPAL** na qual **VAMOS SOLICITAR** o **PULL REQUEST** das nossas **ALTERAÇÕES** posteriormente.
- Então para isso, nós **PRECISAMOS VOLTAR** para a nossa **BRANCH PRINCIPAL** na nossa **MÁQUINA LOCAL**, **ATUALIZAR** os **COMMITS LOCAIS** em **RELAÇÃO** aos **COMMITS** do nosso **GITHUB**, depois **VOLTAR** para a nossa **FEATURE BRANCH** e então **REALIZAR** o **MERGE** da nossa **FEATURE BRANCH** em **RELAÇÃO** a nossa **BRANCH PRINCIPAL** (caso haja necessidade, ou seja, caso de fato haja novos commits para serem atualizados).
- Porém como nós **TEMOS ALTERAÇÕES PENDENTES** para **SEREM COMMITADAS** na nossa **FEATURE BRANCH**, nós **NÃO CONSEGUIREMOS** apenas **VOLTAR** para a nossa **BRANCH PRINCIPAL** para **REALIZAR** esta **ATUALIZAÇÃO** sem que **ENVIEMOS** o **COMMIT** das nossas **ALTERAÇÕES**.
- Mas **NÃO É** isso que nós **QUEREMOS**, pois nós **QUEREMOS** que antes de **COMMITAR** as nossas **ALTERAÇÕES**, nós **PRECISAMOS GARANTIR** que a nossa **BRANCH PRINCIPAL** e a **FEATURE BRANCH** elas **ESTÃO ATUALIZADAS** em **RELAÇÃO** ao **GITHUB**, e também **SEM CONFLITOS**.
- Para isso, nós **PRECISAMOS REALIZAR** o **BACKUP** das nossas **ALTERAÇÕES** da **FEATURE BRANCH** para que **SEJA POSSÍVEL** nós **VOLTARMOS** para a **BRANCH PRINCIPAL** e então **ATUALIZAR** a **BRANCH PRINCIPAL** em **RELAÇÃO** ao nosso **GITHUB**.
- A **SEQUENCIA** de **COMANDO** ficará assim:

```bash
git stash push -m "Descrição das alterações"
git checkout main
git pull origin main
git checkout dev/rafael
git merge main
git stash pop # Este comando pode gerar conflito, e caso aconteça, nós precisaremos resolver este conflito manualmente, escolhendo qual das versões nós desejamos utilizar
```
