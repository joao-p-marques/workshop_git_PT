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

Existe, depois, o conceito de **merge**, que consiste em juntar o trabalho de duas *branches* diferentes numa.

No GitHub (e noutros sistemas), podemos fazer um **Pull Request**, que é um pedido para fazer merge *online*. É útil quando trabalhamos numa equipa, e queremos que as nossas alterações sejam aprovadas por outros.

*Nota:*
Para ver um gráfico com os commits: `git log --graph [--oneline]`

#### Fork

Quando temos um repositório remoto, podemos fazer um **fork** do mesmo.

Ao fazer isso, vamos criar um repositório que será **nosso**, e uma cópia do repositório do qual fizemos o *fork* no momento.

Através disso, podemos desenvolver à parte do repositório principal, e mais tarde juntar o trabalho. Este sistema é muito usado no desenvolvimento **open source**, onde muitas pessoas (desconhecidas) podem trabalhar no mesmo projeto, e sugerir alterações.

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

2. **Criar um repositório**

3. **Seguir as instruções para clonar o repositório**

### Usar o GIT localmente

O git vem instalado por defeito na maioria dos sistemas **linux**.
Em **Windows**, podem instalar [Git Bash](https://git-scm.com/downloads)(sistema básico para o git) o ou [Windows Subsystem for Linux(WSL)](https://docs.microsoft.com/en-us/windows/wsl/install-win10)(terminal linux no windows, uma boa opção para ter acesso a outros recursos do linux).

4. **Adicionar informação ao README**.
Um ficheiro `README.md` é criado por defeito (ou pode ser criado depois). Vamos adicionar alguma coisa a esse ficheiro. Por exemplo: `Primeiro repositório git`.

5. **Fazer commit e push das alterações**
Usando os comandos `git add -A`, `git commit -m "primeiro commit"` e `git push origin master`, enviamos a informação para o servidor git.

### Usar cliente GIT com GUI

Em vez de usar a linha de comandos, podemos usar uma interface gráfica(GUI) para controlar o GIT, como o [GitHub Desktop](https://desktop.github.com/).

Podemos executar os mesmos comandos que na linha de comandos, ou visualizar a informação.

### Usar a integração GIT de um IDE

6. **Clonar o repositório num IDE que tenha integração GIT**
A maioria dos *Integrated Development Environment*(IDE) têm integração com o git. Se abrirmos os Visual Studio (usado para C#, por exemplo), podemos usá-lo para aceder e usar os repositórios git.podemos usá-lo para aceder e usar os repositórios git.

No VS, vamos a Team > Manage Connections e vemos uma barra à direita com opções de integração com Git.
