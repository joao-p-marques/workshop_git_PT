# Workshop GIT

Guia para workshop GIT (PT)

## 1. Controlo de versões

**O que é?** Gestão de diferentes versões de determinados documentos, ou pastas. Envolve a gestão de trabalho *ao longo do tempo* e *para uma equipa a trabalhar no mesmo projeto*.

**Exemplos:** Google Docs (permite que várias pessoas editem o mesmo documento ao mesmo tempo)

Normalmente deve permitir identificar **quem** fez **o quê** e **quando**, e **reverter** alterações que causaram problemas, bem como **juntar** diferentes alterações feitas por várias pessoas ao mesmo tempo.

## 2. GIT

Git é um protocolo que aplica a gestão de versões.

Foi criado em 2005 por **Linus Torvalds**, o criador do **Linux**, e tem sido melhorado deste então. Veio resolver o problema que tinha de gerir muito código, escrito por muitas pessoas ao mesmo tempo.

Hoje é usado em quase todos os projetos de software.

Pode parecer difícil para novos utilizadores... Mas:
* tem ~200 comandos
* podemos começar a usar bem o sistema com menos de 12

### Vantagens:
* Eficiencia de espaço no disco
* Muito melhor que outros métodos (mandar código por e-mail...)
* Muito fácil para **juntar** e **migrar** código
* Seguro
* Muitas ferramentas construídas à volta do git(**GitHub**, ...)

### Conceitos do Git:

#### Commit

É uma **alteração** em 1 ou mais ficheiros, associada a uma **mensagem** explicativa...

![Commit workflow](https://github.com/joao-p-marques/workshop_git_PT/raw/master/images/commit.png "Commit workflow")

#### Branch

É uma **sequência de commits**.

Normalmente cada branch corresponde a um **incremento** específico no trabalho(corrigir um bug, adicionar uma funcionalidade, ...)

![Branch workflow](https://github.com/joao-p-marques/workshop_git_PT/raw/master/images/branches.png "Branch workflow")

Ao criar um repositório, começamos com a *branch* **master**, e partimos daí.

#### Remote

Repositório/servidor git remoto.

Localmente temos um repositório git que funciona para gerir o nosso trabalho.

Normalmente, para trabalhar em equipa, publicar o trabalho, ou para ter uma cópia, queremos armazená-lo noutro sítio: um **servidor remoto**.

O servidor principal onde armazenamos os dados chama-se **origin**, mas podemos adicionar outros.

![Remotes workflow](https://github.com/joao-p-marques/workshop_git_PT/raw/master/images/remotes.png "Remotes workflow")

Exemplos: **GitHub**, **GitLab**, ...

## 3. Prática

### Comandos Git

#### Inicializar repositório

`git init` para inicializar um repositório (local).

`git clone <url>` para "clonar" um repositório remoto(GitHub, etc.) para um repositório local.

#### Commit

`git add <EXPR>` para **adicionar** as mudanças ao git (para que ele as "conheça").
EXPR pode ser o nome de um ficheiro, pasta, ..., ou `-A` para adicionar tudo.

`git commit` para fazer o commit das mudanças adicionadas. Abre um editor de texto para escrever a mensagem de commit.

*Outros comandos:*
`git status`
`git stash`
`git log`
`git diff`

#### Branches

`git branch <NOME>` para criar uma branch nova. 

`git checkout <NOME>` para mudar para branch existente.

*Nota:*
`git checkout -b <NOME>` cria e, ao mesmo tempo, muda para uma nova branch.

Ao criar uma branch, podemos especificar a branch de origem. Por defeito é atual.

`git merge <NOME>` para fazer "merge" dos commits da branch "NOME" para a branch atual.

Algumas destas operações podem ser realizadas facilmente diretamente na interface gráfica do repositório do GitHub.

#### Remotes

Gerir os repositórios remotos.

`git remote add origin <URL>` adiciona um repositório remoto com a etiqueta **origin**(etiqueta por defeito de qualquer repositório) para um URL. (Se tivermos feito clone o URL é configurado automaticamente)

`git push origin master` envia os commits locais para o remote **origin**, da branch **master**.

`git pull origin master` para obter os commits do remote.

### GitHub

1. **Criar conta no GitHub**
Ir a ao site do [GitHub](https://github.com/) e criar uma conta.
