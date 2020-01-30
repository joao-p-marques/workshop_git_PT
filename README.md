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
